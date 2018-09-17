[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

    import scipy.stats
    
    mu = 178
    sigma = 7.7
    dist = scipy.stats.norm(loc=mu, scale=sigma)
    type(dist)
    
    dist.mean(), dist.std()
    
    dist.cdf(mu-sigma)
    
5'10" and 6'1" are 177.8 and 185.42cm  
For the solution, find the percentage in that range and multiply by the US male population

    low = dist.cdf(177.8) #percent of people this height or shorter
    high = dist.cdf(185.4) 
    print(high-low)
    
34.2% of men fall in this range  
There are 159.68 million men in the us according to the 2017 US census  
There are around 54,610,560 men in the us are between 5'10" and 6'1".
