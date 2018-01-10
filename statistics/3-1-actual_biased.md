[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 

**Code**  
import nsfg  
import thinkstats2  
import numpy as np  

df = nsfg.ReadFemResp()  
NumKid = df.numkdhh  
pmf = thinkstats2.Pmf(np.array(NumKid),label='Actual')  

#Function to calculate the biased distribution  
def BiasPmf(pmf, label):  
    new_pmf = pmf.Copy(label=label)  
    for x, p in pmf.Items():  
        new_pmf.Mult(x, x)  
    new_pmf.Normalize()  
    return new_pmf  

pmfBias = BiasPmf(pmf,'Biased')  

#calculate means  
print('Actual average number of children per home is {0:.2f}; biased value is {1:.2f}'.format(pmf.Mean(),pmfBias.Mean()))
  
thinkplot.PrePlot(2)  
thinkplot.Pmfs([pmf,pmfBias])  
thinkplot.Show(xlabel='Number of Childern', ylabel='PMF')  

**Output**  
*Actual average number of children per home is 1.02; biased value is 2.40*  

**Plot**  
![plot](statistics/Figure_C3E1.png)  

