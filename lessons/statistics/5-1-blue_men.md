[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

#### The percentage of men who are 5'10 or shorter:
```
five_ten = dist.cdf(2.54*(5*12+10))
five_ten
```
0.48963902786483265


#### The percentage of men who are 6'1 or shorter:
```
six_one = dist.cdf(2.54*(6*12+1))
six_one
```
0.8323858654963072


#### To find the percentage of men between 5'10 and 6'1, subtract the former from the latter:
```
ans = six_one - five_ten
ans
```
0.34274683763147457
