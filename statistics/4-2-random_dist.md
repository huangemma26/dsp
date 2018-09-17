[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

    import numpy as np  
    import thinkplot  
    data = np.random.random(1000)
    
    pmf = thinkstats2.Pmf(data)
    thinkplot.Pmf(pmf)
    thinkplot.Config(xlabel='Random Number', ylabel='PMF')

Each point in the graph of the PDF has a uniform height, at 0.001. This is because it shows the probability of each randomly generated number, and they will all have probabilites of 1/1000.

    cdf = thinkstats2.Cdf(data)
    thinkplot.Cdf(cdf)
    thinkplot.Config(xlabel='Random Number', ylabel='CDF', loc='upper left')

The graph of the CDF shows an almost perfect line with a slope of one. This shows the numbers are most likely completely randomly generated, because there is a uniform increase in probability that the number will be less than or equal to a given number as the numbers increase.
