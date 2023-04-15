---
title: Determine the level of significance (p-value) for scikit-learn's linearregression model
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Scikit-learn`s LinearRegression model does not provide p-values for coefficients, but we can calculate them using statsmodels library.
---

**Contents**

[TOC]

## Introduction

Linear regression is a popular technique for modeling the relationship between a dependent variable and one or more independent variables. The scikit-learn library in Python provides a LinearRegression class that can be used to fit linear regression models to data using least squares.

When fitting a linear regression model, it is important to evaluate the significance of the model and its coefficients. The p-value is a statistical measure that indicates the probability of observing a test statistic as extreme as the one computed from the data, assuming that the null hypothesis is true. In the case of linear regression, the null hypothesis is that the slope of the regression line is zero.

In this tutorial, we will discuss how to calculate the p-value in scikit-learn LinearRegression in Python.

## Import Libraries

We start by importing the required libraries for our analysis. First, we need to import the LinearRegression class from scikit-learn. We also need to import numpy and pandas for data manipulation and matplotlib for data visualization.

```
from sklearn.linear_model import LinearRegression
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

## Generate Data

Next, we need to generate some data to fit our linear regression model. We will simulate data with a linear relationship between two variables, X and y.

```
np.random.seed(0)
n_samples = 100
X = np.random.rand(n_samples)
y = 2*X + np.random.rand(n_samples)
```

## Fit Linear Regression Model

We can now fit a linear regression model to the data using the LinearRegression class from scikit-learn.

```
lr = LinearRegression()
lr.fit(X.reshape(-1,1), y)
```

We reshape the X array to ensure that it is a two-dimensional array with a single column, which is required by the fit method.

## Calculate P-Value

Finally, we can calculate the p-value for the slope coefficient of the linear regression model using the statsmodels library. The statsmodels library provides a convenient way to perform statistical tests, including the t-test used to calculate the p-value.

```
import statsmodels.api as sm

X2 = sm.add_constant(X.reshape(-1,1))
est = sm.OLS(y, X2)
est2 = est.fit()
print(est2.summary())
```

The summary method of the OLS results object provides a table of statistical tests for the linear regression model, including the t-test for the slope coefficient and its corresponding p-value. The p-value is reported in the column labeled "P>|t|" and should be compared to a chosen significance level (e.g., 0.05) to determine whether the coefficient is statistically significant or not.

## Conclusion

In this tutorial, we discussed how to calculate the p-value in scikit-learn LinearRegression in Python. We generated some simulated data, fit a linear regression model using the LinearRegression class from scikit-learn, and calculated the p-value for the slope coefficient using the statsmodels library. The p-value is a measure of the significance of the model and its coefficients, and can be used to determine whether the model is statistically significant or not.
