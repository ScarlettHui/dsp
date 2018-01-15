[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

**code**  
```
import scipy.stats  
#convert the blueman height standard numbers to cm  
h1 = (5*12+10)*2.54  
h2 = (6*12+1)*2.54  
#calculate the CDF at the two boundary points so as to calculate the percentage in between  
cdf1 = scipy.stats.norm.cdf(h1,loc=178,scale=7.7)  
cdf2 = scipy.stats.norm.cdf(h2,loc=178,scale=7.7)  
print('The percentage of US male that in the Blueman height range is: {:.1%}'.format(cdf2-cdf1))  
```

**output**  
_The percentage of US male that in the Blueman height range is: 34.3%_  
