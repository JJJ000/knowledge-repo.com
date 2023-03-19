---
title: The task involves employing numpy for creating an array that contains all possible combinations of two arrays
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use numpy.meshgrid() to build an array of all combinations of two arrays in Python.
---

**Contents**

[TOC]

### Section 1: The Problem Statement

Given two arrays A and B of different lengths, we want to create an array C containing all possible combinations of elements from A and B.

For example, if A = [1, 2] and B = [3, 4, 5], the resulting array C would be:

```
C = [[1, 3], [1, 4], [1, 5], [2, 3], [2, 4], [2, 5]]
```


### Section 2: Using NumPy to build the array of combinations

To build the array of all combinations of two arrays in Python, we can use NumPy's `meshgrid` function. 

Here's how it works:

```python
import numpy as np

A = np.array([1, 2])
B = np.array([3, 4, 5])

AA, BB = np.meshgrid(A, B)
C = np.stack((AA.ravel(), BB.ravel()), axis=1)
```

The `meshgrid` function creates two 2D arrays `AA` and `BB` containing all possible combinations of elements from `A` and `B`, respectively.

The `ravel` function then flattens the 2D arrays into 1D arrays, so that we can stack them together using NumPy's `stack` function. The `axis=1` argument tells `stack` to stack the arrays horizontally.

The resulting array `C` is the desired array containing all possible combinations of elements from `A` and `B`.


### Section 3: Example

Here's an example showing how to use the above code to create an array of all combinations of two arrays:

```python
import numpy as np

# initialize input arrays
A = np.array([1, 2])
B = np.array([3, 4, 5])

# build array of all combinations
AA, BB = np.meshgrid(A, B)
C = np.stack((AA.ravel(), BB.ravel()), axis=1)

# print resulting array
print(C)
```

Output:
```
[[1 3]
 [2 3]
 [1 4]
 [2 4]
 [1 5]
 [2 5]]
```


### Section 4: Conclusion

In this tutorial, we explored how to use NumPy's `meshgrid` function to create an array of all possible combinations of elements from two input arrays in Python. We accomplished this by first using `meshgrid` to create two 2D arrays of all possible combinations, then flattening those arrays and stacking them horizontally using NumPy's `ravel` and `stack` functions. This approach is simple and efficient, and can be used to build arrays of all possible combinations of two or more input arrays in Python.
