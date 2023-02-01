---
title: What is the numpy function for finding the first occurrence of an element in an array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, the NumPy function `np.argwhere()` can be used to return the first index of something in an array in Python.
---

**Contents**

[TOC]

**Yes: `numpy.argmax()`**

### Overview

`numpy.argmax()` is a NumPy function that returns the first index of an item in an array. It is a powerful tool for finding the index of a particular element in an array, and can be used in many different types of applications.

### Syntax

The syntax for `numpy.argmax()` is as follows:

```python
numpy.argmax(array, axis=None, out=None)
```

### Parameters

The `array` parameter is the array in which the index of the element is to be found. The `axis` parameter is an optional parameter that specifies the axis along which to search for the element. The `out` parameter is an optional parameter that specifies the output array.

### Examples

Here are some examples of how `numpy.argmax()` can be used:

```python
# Find the index of the maximum element in a 1-D array
import numpy as np
arr = np.array([1, 5, 3, 8, 9, 4])
index = np.argmax(arr)
print(index) # Outputs 4

# Find the index of the maximum element in a 2-D array
arr = np.array([[1, 5, 3], [8, 9, 4]])
index = np.argmax(arr, axis=1)
print(index) # Outputs [2, 1]
```
