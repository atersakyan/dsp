[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> REPLACE THIS TEXT WITH YOUR RESPONSE
# Plot CDF for rands
rands_cdf = thinkstats2.Cdf(rands)
thinkplot.Cdf(rands_cdf)
thinkplot.Show(xlabel='percentile rank', ylabel='CDF')

## This gives a normal looking gradual line upwards

# PMF for rands
pmf_rands = thinkstats2.Pmf(rands)
#thinkplot.PrePlot(1)
thinkplot.Pmf(pmf_rands)
thinkplot.Show()

## This gives an unclear graph
