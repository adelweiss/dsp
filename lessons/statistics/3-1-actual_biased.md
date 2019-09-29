[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

    import nsfg
    import thinkstats2
    import thinkplot

    resp = nsfg.ReadFemResp()
    actual_pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')

    def BiasPmf(pmf, label):
        new_pmf = pmf.Copy(label=label)

        for x, p in pmf.Items():
            new_pmf.Mult(x, x)

        new_pmf.Normalize()
        return new_pmf

    biased_pmf = BiasPmf(pmf_actual, label='biased')

    thinkplot.PrePlot(2)
    thinkplot.Pmfs([actual_pmf, biased_pmf])
    thinkplot.Show(xlabel='no. of children', ylabel='PMF')

    print('actual mean', actual_pmf.Mean())
    print('biased mean', biased_pmf.Mean())
