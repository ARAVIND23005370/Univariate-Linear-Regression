# Implementation of Univariate Linear Regression
## Aim:
Implement univariate Linear Regression to fit a straight line using the least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line to best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y-intercept of the line using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y-intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
# Develpoed by:PRAVIN KUMAR A
# Register number:212223230155
import numpy as np
import matplotlib.pyplot as plt
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean=np.mean(x)
ymean=np.mean(y)
num=0
den=0
for i in range(len(x)):
  num+=(x[i]-xmean)*(y[i]-ymean)
  den+=(x[i]-xmean)**2
m=num/den
b=ymean-m*xmean
print(m,b)
ypred=m*x+b
print(ypred)
plt.scatter(x,y,color="Red")
plt.plot(x,ypred,color="Blue")
plt.show()
```
## Output
![EX009](https://github.com/RAVENPRAVIN/Univariate-Linear-Regression/assets/146820534/2e422fb6-c60a-423c-96b5-867cb8ebd13e)
![EX09](https://github.com/RAVENPRAVIN/Univariate-Linear-Regression/assets/146820534/7f8568dc-fe4c-4236-99c8-eb16197ec6c3)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
