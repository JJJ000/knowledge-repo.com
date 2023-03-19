---
title: Simultaneous determination of maximum and minimum values through a numpy function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The function np.ptp() returns the range (max-min) of values of a NumPy array in a single function call.
---

**Contents**

[TOC]

Introduction to NumPy

NumPy is a Python library that provides multi-dimensional arrays, linear algebra functions, Fourier transforms, and random number capabilities. NumPy is short for "Numerical Python." It is a fundamental library used by scientists and data analysts in Python.

Simultaneous max() and min()

Sometimes, it’s necessary to get the maximum and minimum values of an array simultaneously. Fortunately, NumPy provides a function that accomplishes this. The function is named `ptp()`.

Section 1: What is the ptp() function in NumPy?

The `ptp()` function in NumPy returns the peak-to-peak (maximum-minimum) value of the input array along with the indices of the highest and the lowest values of an array in a tuple. The function works for both single and multi-dimensional arrays.

Syntax: `numpy.ptp(array, axis=None, out=None, keepdims=<no value>)`

Section 2: Examples of Using ptp() Function in NumPy for Maximum and Minimum

Example 1: For a multi-dimensional array in NumPy

```
import numpy as np
arr1 = np.array([[0, 5], [1, 3]])
print(arr1.ptp()) # Output: 5
```

Example 2: For a single-dimensional array in NumPy

```
import numpy as np
arr2 = np.array([5, 0, 9, 4, 6, 2])
print(arr2.ptp()) # Output: 9
```

Example 3: For a specified axis in a multi-dimensional array in NumPy

```
import numpy as np
arr3 = np.array([[0, 5], [1, 3]])
print(arr3.ptp(axis=0)) # Output: [1 2]
```

In the third example, the `ptp()` function returns a one-dimensional array of shape `(2,)` with the maximum and minimum values along each column of the input array.

Section 3: Conclusion

NumPy’s `ptp()` function is the most suitable for finding both the maximum and minimum values in a multi-dimensional Python array. With `ptp()`, it’s possible to calculate the max and min values and their indices simultaneously.
