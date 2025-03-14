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
Developed by: Prathiksha R
RegisterNumber: 212224040244 
*/
import numpy as np

import matplotlib.pyplot as plt x=np.array(eval(input()))

y=np.array(eval(input()))

mean_x=np.mean(x)

mean_y=np.mean(y)

num_m=0

den_m=0

for i in range(len(x)):

num_m+=(x[i]-mean_x)*(y[i]-mean_y)

den_m+=(x[i]-mean_x)**2
m=num_m/den_m

b=mean_y - m*mean_x

yi=m*x+b

print("Mean of x:",mean_x) print("Mean of y:",mean_y) print("Value of m:",m) print("Value of b:",b)

plt.scatter(x,y) plt.plot(x,yi,"yellow") plt.show()
```

## Output:
![best fit line](sam.png)

![Screenshot 2025-03-08 131836](https://github.com/user-attachments/assets/d313ded7-c423-4fe2-8e87-15ce9b592148)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
