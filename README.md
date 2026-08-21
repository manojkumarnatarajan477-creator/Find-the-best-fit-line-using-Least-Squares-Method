# Implementation of Univariate Linear Regression
## NAME: MANOJ KUMAR N
## REG NO: 212225230168

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
```python

import numpy as np
import matplotlib.pyplot as plt

# Input data
X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 4, 5, 4, 5])

# Calculate means
x_mean = np.mean(X)
y_mean = np.mean(Y)

# Calculate slope (m)
m = np.sum((X - x_mean) * (Y - y_mean)) / np.sum((X - x_mean) ** 2)

# Calculate intercept (c)
c = y_mean - m * x_mean

# Predict Y values
Y_pred = m * X + c

# Display results
print("Slope (m) =", m)
print("Intercept (c) =", c)
print("Linear Regression Equation: Y =", m, "X +", c)

# Plot the data and regression line
plt.scatter(X, Y,color="red",label="Actual Data")
plt.plot(X, Y_pred , color="blue", label="Regression Line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.show()

```

## Output:
<img width="1084" height="698" alt="image" src="https://github.com/user-attachments/assets/9a1565ec-54e6-4463-bb9b-98a593adcda5" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
