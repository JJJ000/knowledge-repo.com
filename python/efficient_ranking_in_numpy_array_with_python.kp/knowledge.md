---
title: Devising a python/numpy program to assign rankings to elements in an array without requiring two sorting operations
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: Use `argsort()` method in NumPy to get the indices that would sort the array and then use these indices to rank the original array.
---

**Contents**

[TOC]

1. Introduction:

In data science, we often need to rank items in an array. While NumPy provides several built-in functions to sort an array, sorting an array twice to obtain the ranks can lead to a considerable computational overhead. In this tutorial, we will discuss different ways to rank items in an array using Python/NumPy without sorting an array twice.

2. Method 1: Using argsort() and argsort().argsort():

The first method to rank items in an array using Python/NumPy involves using the argsort() function to obtain the indices of the sorted elements, and then applying argsort() function again to obtain the ranks. Here's how to implement this method:

``` python
import numpy as np

arr = np.array([3, 1, 4, 2])
sorted_indices = np.argsort(arr)
ranks = np.argsort(sorted_indices)
```

The above code creates an array `arr` and obtains the indices of the sorted elements using the `argsort()` function. These sorted indices are then sorted again to obtain the ranks.

3. Method 2: Using lexsort():

The second method to rank items in an array using Python/NumPy involves using the `lexsort()` function. Here's how to implement this method:

``` python
import numpy as np

arr = np.array([3, 1, 4, 2])
ranks = np.lexsort((arr,))
```

The above code creates an array `arr` and applies the `lexsort()` function to it. The `lexsort()` function sorts the array by columns or rows, and the tuple `(arr,)` specifies that we want to sort the array by the first column (i.e. `arr`). The resulting `ranks` array contains the indices of the sorted elements, which represent the ranks.

4. Conclusion:

In conclusion, there are several ways to rank items in an array using Python/NumPy, without sorting an array twice. We have discussed two such methods in this tutorial - using `argsort()` function twice and using `lexsort()` function. While both methods are efficient, the `lexsort()` function provides a more concise way to obtain the ranks.
