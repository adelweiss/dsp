[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

    import numpy as np 
    import thinkstats2
    import thinkplot

    sample = np.random.random(1000)

    pmf = thinkstats2.Pmf(sample)
    thinkplot.Pmfs([pmf])
    thinkplot.Show(xlabel='random numbers', ylabel='PMF')

    cdf = thinkstats2.Cdf(sample)
    thinkplot.Cdf(cdf)
    thinkplot.Show(xlabel='random numbers', ylabel='CDF')

>>> The distribution appears to be uniformed, from the pmf plot, each numbers appears to have an equal probability of selection. Moreover the cdf plot is close to a straight line along the diagonal (x=y) of the graph. 
