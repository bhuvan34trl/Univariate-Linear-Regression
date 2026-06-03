# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.<img width="1600" height="927" alt="aaaa" src="https://github.com/user-attachments/assets/94b31691-6969-4f38-b75b-936db9965cab" />

#Developerd by:Bhuvanesh.K
#RegisterNumber: 212225230035

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
   num+=(x[i]-xmean)*(y[i]-ymean)
   den+=(x[i]-xmean)**2

m = num/den
b = ymean m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y, color='Red')
plt.plot(x,ypred, color='Blue')
plt.show()






```
## Output
<img width="1600" height="927" alt="aaaa" src="https://github.com/user-attachments/assets/4615bd49-b7d6-4482-a7cf-cde276b52865" />


<img width="822" height="647" alt="image" src="https://github.com/user-attachments/assets/6c33f8c7-2b82-4809-8c16-7c0cc44e2c1b" />

<img width="947" height="555" alt="image" src="https://github.com/user-attachments/assets/bf046677-c87b-40de-b68a-c0e7333a6895" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
