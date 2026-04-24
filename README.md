# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Mohamed Hafees R
RegisterNumber:  212225230175
*/
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
xmean=np.mean(x)
ymean=np.mean(y)
num,den=0,0 
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m=num/den
c=ymean-m*xmean
print(m,c)
y_pred=m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot(x,y_pred,color="red")
plt.show()
```

## Output:
```
 1.1, 1.3, 1.5, 2.0, 2.2, 2.9, 3.0, 3.2, 3.2, 3.7 
 39343, 46205, 37731, 43525, 39891, 56642, 60150, 54445, 64445, 57189 
9020.635598878354 28216.868206703162 
[38139.56736547 39943.69448525 41747.82160502 46258.13940446 
 48062.26652424 54376.71144345 55278.77500334 57082.90212311 
 57082.90212311 61593.21992255]
```

<img width="749" height="517" alt="image" src="https://github.com/user-attachments/assets/9331ac98-644d-4999-a9b3-d7d349c3d12a" />




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
