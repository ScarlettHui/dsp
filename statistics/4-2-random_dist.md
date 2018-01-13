[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

**Code**
```
import numpy as np   
import thinkstats2   
import thinkplot   
#Generate 1000 random numbers   
randNum = np.random.random(1000)   
#Use thrinkstats' author's prebuilt funtions to calculate and plot PMF   
pmf = thinkstats2.Pmf(randNum,label='PMF')   
thinkplot.Pmf(pmf)   
thinkplot.Show(xlabel='Random Number',ylabel='PMF')   
#Use thrinkstats' author's prebuilt funtions to calculate and plot CDF   
cdf = thinkstats2.Cdf(randNum,label='CDF')   
thinkplot.Cdf(cdf)   
thinkplot.Show(xlabel='Random Number',ylabel='CDF')   
```
**Plots**  
![PMF](dsp/img/Figure_C4_PMF.png)  
![CDF](dsp/img/Figure_C4_CDF.png)  
  
**Answer**    
The distribution is uniform: from PMF plot, we can see that the probability for each value is the same 0.001; from CDF plot, we can see that the CDF at each value is equal to the value. Both indicate that the distribution is uniform  
