[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

    print(firsts.totalwgt_lb.mean())  
    print(others.totalwgt_lb.mean())

On average, first babies are lighter than others.

    def CohenEffectSize(group1, group2):  
        diff = group1.mean() - group2.mean()  
        var1 = group1.var()  
        var2 = group2.var()  
        n1, n2 = len(group1), len(group2)  
        pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)  
        d = diff / np.sqrt(pooled_var)  
        return d  
        
    CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

Negative Cohen Effect makes sense as the mean for the firsts total weight is smaller than the others. The difference itself between the is tiny.
