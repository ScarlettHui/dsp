[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>__Code__  
import nsfg  
preg = nsfg.ReadFemPreg()  
live = preg[preg.outcome == 1]  
firsts = live[live.birthord == 1]  
others = live[live.birthord != 1]  
diff = firsts.totalwgt_lb.mean()-others.totalwgt_lb.mean()  
var1 = firsts.totalwgt_lb.var()  
var2 = others.totalwgt_lb.var()  
n1 = len(firsts.totalwgt_lb)  
n2 = len(others.totalwgt_lb)   
pooled_var = (n1*var1 + n2*var2)/(n1+n2)  
d = diff/math.sqrt(pooled_var)  
***With these, Cohen's d is calcuated as -0.088672927072602***
*It indicates that the first born baby is avaragely lighter than the latter ones, yet the difference is quite small, only around 0.0887 standard deviation.*  