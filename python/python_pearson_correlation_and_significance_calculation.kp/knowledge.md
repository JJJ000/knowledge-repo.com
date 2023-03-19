---
title: How to compute pearson's correlation coefficient and statistical significance using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To calculate the Pearson correlation and significance in Python, you can use the `pearsonr` function from the `SciPy` library.
---

**Contents**

[TOC]

Section 1: Introduction

Pearson correlation is a measure of linear correlation between two variables. It measures the strength and direction of the linear relationship between two variables. In statistics, Pearson correlation is denoted by the symbol r. The value of r lies between -1 and +1. A value of +1 indicates a perfect positive linear relationship, while a value of -1 indicates a perfect negative linear relationship. A value of zero indicates that there is no linear relationship between the two variables.

In this article, we will discuss how to calculate Pearson correlation and significance in Python.

Section 2: Calculating Pearson Correlation in Python

To calculate Pearson correlation in Python, we can use the scipy.stats module. Specifically, we can use the pearsonr() function. 

The pearsonr() function takes two arrays or lists as input and returns two values: the Pearson correlation coefficient and the p-value. The p-value is the significance level at which the null hypothesis (that there is no correlation between the two variables) can be rejected.

Here is an example code that shows how to use the pearsonr() function in Python:

```python
from scipy.stats import pearsonr

# create two lists of data
x = [1, 2, 3, 4, 5]
y = [5, 4, 3, 2, 1]

# calculate Pearson correlation
corr, p_value = pearsonr(x, y)

# print the results
print("Pearson correlation coefficient:", corr)
print("p-value:", p_value)
```

The output of this code should be:

```
Pearson correlation coefficient: -1.0
p-value: 0.0
```

This indicates a perfect negative linear correlation between the two variables, with a p-value of zero indicating that this result is highly significant.

Section 3: Interpreting Pearson Correlation Results

As mentioned earlier, the value of the Pearson correlation coefficient (r) ranges from -1 to +1. Here are some general guidelines on how to interpret the results:

- If r is close to +1, it indicates a strong positive linear correlation between the two variables.
- If r is close to -1, it indicates a strong negative linear correlation between the two variables.
- If r is close to zero, it indicates that there is no linear correlation between the two variables.
- The farther away r is from zero (in either direction), the stronger the linear correlation.
- A p-value less than 0.05 is considered statistically significant, which means we can reject the null hypothesis that there is no correlation between the two variables.

Section 4: Conclusion

Pearson correlation is a powerful statistical tool for analyzing the relationship between two variables. In Python, we can easily calculate Pearson correlation and significance using the pearsonr() function in the scipy.stats module. By interpreting the results correctly, we can gain valuable insights into the relationship between two variables and make informed decisions based on the data.
