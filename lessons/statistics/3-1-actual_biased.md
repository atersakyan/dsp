[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> REPLACE THIS TEXT WITH YOUR RESPONSE
# PMF unbiased
pmf_numkdhh = thinkstats2.Pmf(resp.numkdhh, label='actual')
print('mean =', pmf_numkdhh.Mean())
# mean = 1.024205155043831

# Biased PMF
def BiasPmf(pmf_unbias, label):
    new_pmf = pmf_unbias.Copy(label=label)
    for x, p in pmf_unbias.Items():
        new_pmf.Mult(x, x)
    new_pmf.Normalize()
    new_pmf.Mean()
    return new_pmf, new_pmf.Mean()

BiasPmf(pmf_numk, 'biased')
(Pmf({0: 0.0, 1: 0.20899335717935616, 2: 0.38323965252938175, 3: 0.25523760858456823, 4: 0.10015329586101177, 5: 0.052376085845682166}, 'biased'),
 2.403679100664282)

biased_pmf = BiasPmf(pmf, label='observed')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf_numkdhh, biased_pmf])
thinkplot.Show(xlabel='class size', ylabel='PMF')

# Plot won't copy here but in my notebook it is clear that there is a large dif between biased and unbiased PMFs




