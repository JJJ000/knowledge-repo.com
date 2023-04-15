---
title: Discover the indexes of zero-valued components in a numpy matrix
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the np.where() method with a condition of the array being equal to zero to find the indices of elements equal to zero in a NumPy array in Python.
---

**Contents**

[TOC]

# Introduction
In this task, we are required to find the indices of the elements that are equal to zero in a NumPy array. NumPy is a general-purpose array-processing package in Python that provides tools for working with multidimensional arrays. In NumPy, we can find the indices of elements equal to zero easily by using the `np.where()` function. In this tutorial, we will discuss how to find the indices of elements equal to zero in a NumPy array in Python.

# Import Libraries
In order to find the indices of elements equal to zero in a NumPy array, we need to import the necessary libraries. In this case, we need to import NumPy library.

```python
import numpy as np
```

# Find Indices of Elements equal to Zero
NumPy provides the `np.where()` function to find the indices of elements in an array that satisfy a particular condition. We can use this function to find the indices of elements equal to zero in a NumPy array.

```python
arr = np.array([1, 0, 3, 0, 5, 6, 0])

# using np.where() to find indices where elements are equal to zero
res = np.where(arr == 0)

print(res)
```

Output:
```
(array([1, 3, 6]),)
```

In the above code, we first created a NumPy array `arr`, then we used the `np.where()` function to find the indices where elements in the array are equal to zero. The function returned a tuple containing an array of indices of elements that satisfy the condition.

# Conclusion
In this tutorial, we have discussed how to find the indices of elements equal to zero in a NumPy array in Python. We used the `np.where()` function to find the indices of elements that satisfy the condition. We hope you find this tutorial helpful.
