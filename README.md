# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. 
3. Calculate the mean of the X -values and the mean of the Y -values.
4. 
5. Find the slope m of the line of best fit using the formula.
6. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

7. Compute the y -intercept of the line by using the formula:
8. 
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

9. Use the slope m and the y -intercept to form the equation of the line.
10. 
11. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: s.rohith kumar

RegisterNumber:  24004371
*/
import numpy as np

import matplotlib.pyplot as plt

x = np.array(eval(input("Enter the input x: ")))

y = np.array(eval(input("Enter the input y: ")))

print("OUTPUT")

print("x =", x)

print("y =", y)

x_mean = np.mean(x)

y_mean = np.mean(y)

num = 0

denom = 0

for i in range(len(x)):

    num += (x[i] - x_mean) * (y[i] - y_mean)

    denom += (x[i] - x_mean) ** 2

m = num / denom

b = y_mean - m * x_mean


print("Slope:", m, "Intercept:", b)


y_pred = m * x + b

print("y_prediction:", y_pred)
 
plt.scatter(x, y)

plt.plot(x, y_pred, color='blue')

plt.show()
```

## Output:
![best fit line](sam.png)
![Screenshot (9)](https://github.com/user-attachments/assets/98fc0bf3-be20-4355-a096-fd05fcca5d5b)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
