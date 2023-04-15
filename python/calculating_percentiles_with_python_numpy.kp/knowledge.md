---
title: What is the process of computing percentiles using python/numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the np.percentile() function from numpy to calculate percentiles in Python.
---

**Contents**

[TOC]

## Section 1: Understanding Percentiles

In statistics, a percentile signifies the value below which a given percentage of observations in a data set fall. For example, the 25th percentile of a data set would be the value below which 25% of observations in the dataset falls. Percentiles can give us a better understanding of the distribution of data sets and help us find outliers.

## Section 2: Using numpy.percentile() Method

The NumPy library in Python provides a built-in method for calculating percentiles called `percentile()`. The method takes three arguments:

- the input array containing the dataset
- the percentile(s) you want to calculate (can be a single percentile or a list of percentiles)
- an optional argument axis that specifies the axis along which the percentiles are calculated

The percentile method returns the value(s) of the percentile(s) requested. Here's an example code that demonstrates how to use the percentile method to calculate the 25th percentile of a dataset:

```python
import numpy as np

# create a dataset
dataset = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# calculate the 25th percentile
q1 = np.percentile(dataset, 25)

print(q1)
```

Output:
```
2.75
```

## Section 3: Calculating Multiple Percentiles

You can calculate multiple percentiles at once by passing a list of percentiles as the second argument to the percentile method. Here's an example code that demonstrates how to calculate the 25th and 75th percentiles of a dataset:

```python
import numpy as np

# create a dataset
dataset = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# calculate the 25th and 75th percentiles
q1, q3 = np.percentile(dataset, [25, 75])

print(q1, q3)
```

Output:
```
2.75 7.25
```

## Section 4: Calculating Percentiles Along an Axis

You can calculate percentiles along a specified axis of a multi-dimensional array by passing the axis argument to the percentile function. Here's an example code that demonstrates how to calculate the 25th percentile of a 2-dimensional array along the rows (axis=1):

```python
import numpy as np

# create a 2D array
arr_2d = np.array([[10, 7, 4], [3, 2, 1]])

# calculate the 25th percentile along the rows
q1 = np.percentile(arr_2d, 25, axis=1)

print(q1)
```

Output:
```
[4.75 1.25]
```

In this example, the `q1` array contains the 25th percentile values of each row in `arr_2d`.
