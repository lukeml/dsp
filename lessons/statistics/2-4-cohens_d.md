[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)


We're supposed to say something about whether first babies are lighter or heavier than others.
We can repeat a bit of what was done for length. 
However, to say anything useful, we'd probably want to do a paired t test or something like that. 
But we haven't discussed that yet at this point in the text.

Means of total weight in pounds for firsts, others
```
print(firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean())
```

Difference of those means 
```
print(firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean())
```

Difference is negative, so we might be tempted to say first babies are lighter in weight. 
However, we can't say anything about the significance. 
We can calculate individual variances or standard deviations for both groups, but that on its own doesn't tell us much.

Standard deviations of total weight in pounds for firsts, others
```
print(firsts.totalwgt_lb.std(), others.totalwgt_lb.std())
```

We can also calculate Cohen's d for these two using the provided function.
```
cohen_prg_wt = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
print(cohen_prg_wt)
```

This is also negative, although it's a fairly small standardized value.
However, the text doesn't actually give guidelines. 
Online searches say "medium" values range from 0.5 to 0.8. 
So a value of -0.089 probably doesn't allow one to draw any conclusions.
We'd want to do a paired t test or something like that to at least get a p-value.
