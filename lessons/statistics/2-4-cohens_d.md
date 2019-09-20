[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> REPLACE THIS TEXT WITH YOUR RESPONSE

#Cohens d = difference between groups to the variability within groups.
#d = (Mean Group 1 - Mean Group 2)/ (Pooled stdv i.e avg stdv of the groups)
#SDpooled = √((SD1^2 + SD2^2) ⁄ 2

# I used stdv pooled using the equation above rather than the author's use of variance pooled

# Get filters for weights of firsts vs others
# total weight in lb for Firsts
firsts_weight = firsts['totalwgt_lb']
# total weight in lb for Others
others_weight = others['totalwgt_lb']

def CohensD(group1, group2):
    ''' Fx to compute Cohen's d effect size'''
    import math
    mean_diff = group1.mean() - group2.mean()
    stdv_grp1 = group1.std()
    stdv_grp2 = group2.std()
    std_pooled = math.sqrt((stdv_grp1**2 + stdv_grp2**2)/2)
    d = mean_diff/std_pooled
    return d

CohensD(firsts_weight, others_weight)
# -0.08864367587767744, this is a very weak effect size. You can look at the descriptives to further examine the direction (negative) / difference between group
