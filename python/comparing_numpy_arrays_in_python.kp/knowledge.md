---
title: Checking if two numpy arrays are the same, element by element
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To compare two NumPy arrays element-wise for equality, use the numpy.array\_equal() function.
---

**Contents**

[TOC]

## Using np.array_equal()
The simplest way to compare two NumPy arrays for equality is to use the np.array_equal() function. This function returns True if two arrays have the same shape and elements, False otherwise. 

Example:
```
import numpy as np

a = np.array([1,2,3])
b = np.array([1,2,3])

np.array_equal(a,b)
```
Output: True

## Using np.allclose()
The np.allclose() function is another way to compare two NumPy arrays for equality. This function returns True if two arrays are element-wise equal within a tolerance.

Example:
```
import numpy as np

a = np.array([1,2,3])
b = np.array([1,2,3.1])

np.allclose(a,b)
```
Output: True
