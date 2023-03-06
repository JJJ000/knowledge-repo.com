---
title: Discovering distinct rows in a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use np.unique(arr, axis=0) to find unique rows in a numpy array arr.
---

**Contents**

[TOC]

## Introduction
NumPy is a fundamental package for scientific computing in Python. It provides a powerful array object that can be used for different purposes, including storing and manipulating data. One common task is finding unique rows in an array. This can be done with a few lines of code using built-in functions provided by NumPy.

In this article, we will explore how to find unique rows in a NumPy array in Python, discussing two different methods to achieve this task.

## Method 1: Using numpy.unique() function
The `numpy.unique()` function can be used to find the unique elements in an array. When applied to a two-dimensional array, it returns the unique rows in the array, which can be exactly what we need to find unique rows. Here's an example of how to use `numpy.unique()` to find unique rows in an array:

```
import numpy as np

a = np.array([[1, 2], [3, 4], [1, 2], [5, 6]])
unique_a = np.unique(a, axis=0)

print(unique_a)
```

Output:
```
[[1 2]
 [3 4]
 [5 6]]
```

As you can see, `numpy.unique()` returned an array with three unique rows, which are the rows that appear in `a` only once.

## Method 2: Using numpy.vstack() and numpy.unique() functions
Another method to find unique rows in a NumPy array is to use the `numpy.vstack()` function to stack the rows of the array vertically and then apply the `numpy.unique()` function to the resulting array. Here's an example of how to use these functions:

```
import numpy as np

a = np.array([[1, 2], [3, 4], [1, 2], [5, 6]])

# stack the rows vertically
stacked_a = np.vstack({tuple(row) for row in a})

# find unique rows
unique_a = np.unique(stacked_a, axis=0)

print(unique_a)
```

Output:
```
[[1 2]
 [3 4]
 [5 6]]
```

In this case, we created a set of tuples using the rows of `a` and then stacked them vertically using `numpy.vstack()`. The resulting array contained the unique rows of `a`, which we identified using `numpy.unique()`.

## Conclusion
Finding unique rows in a NumPy array in Python can be accomplished using different methods. The `numpy.unique()` and `numpy.vstack()` functions are two of the most common methods, providing efficient solutions to this task. By applying these functions, it is easy to extract the unique rows from a large dataset, which can be essential for many data science applications.
