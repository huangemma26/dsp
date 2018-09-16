[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

    resp = nsfg.ReadFemResp()
    
    pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
    
    thinkplot.Hist(pmf)  
    thinkplot.Config(xlabel='number of children', ylabel='PMF')
    
    def BiasPmf(pmf, label):  
       new_pmf = pmf.Copy(label=label)

       for x, p in pmf.Items():  
           new_pmf.Mult(x, x)
        
       new_pmf.Normalize()  
       return new_pmf
       
    biased_pmf = BiasPmf(pmf, label='observed')  
    thinkplot.PrePlot(2)  
    thinkplot.Pmfs([pmf, biased_pmf])  
    thinkplot.Config(xlabel='number of children', ylabel='PMF')
    
    print(pmf.Mean())  
    print(biased_pmf.Mean())
    
 The actual mean is around 1.4 children less than the observed mean, which is around 2.4. This is a huge difference.
