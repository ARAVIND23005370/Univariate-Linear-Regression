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
![RR](https://github.com/RAVENPRAVIN/Univariate-Linear-Regression/assets/146820534/b4a330ac-28ba-4fca-95d0-e62008feaf3d)
4.	Compute the y-intercept of the line using the formula:
  ![RRR](https://github.com/RAVENPRAVIN/Univariate-Linear-Regression/assets/146820534/7e5bb4c4-cfed-4079-828c-1e8e0cdb120b)
5.	Use the slope m and the y-intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
# Develpoed by:ARAVIND R
# Register number:23005370
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
![Screenshot 2023-12-28 221604](https://github.com/ARAVIND23005370/Univariate-Linear-Regression/assets/148514836/cff722c4-051b-4684-90fc-f1cd3c5c6ef9)

![EX09](https://github.com/RAVENPRAVIN/Univariate-Linear-Regression/assets/146820534/afe65a45-dbce-4140-a524-0042e6bce253)
![EX009 (2)](https://github.com/RAVENPRAVIN/Univariate-Linear-Regression/assets/146820534/f06ba21a-3f3d-450c-8322-5f0000b56e27)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
