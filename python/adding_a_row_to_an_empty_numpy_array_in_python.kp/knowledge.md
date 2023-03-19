---
title: What is the process of adding a new row to a numpy array that is empty?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the numpy method `numpy.append(arr, values, axis=0)` to append a new row to an empty numpy array.
---

**Contents**

[TOC]

## Creating an Empty Numpy Array
We can create an empty numpy array using the `numpy.zeros()` function. We can specify the shape of the array and the data type of its elements. For example, to create an empty 2x3 array of type `int`, we can do the following:

``` python
import numpy as np
a = np.zeros((2,3), dtype=int)
```

## Appending a Row to an Existing Numpy Array
To append a row to an existing numpy array, we can use the `numpy.append()` function. We need to pass the array and the row to be appended as arguments to the function. Let's say we want to append the row `[4, 5, 6]` to the array `a`. We can do the following:

``` python
row_to_append = np.array([4,5,6])
a = np.append(a, [row_to_append], axis=0)
```

Here, we pass the argument `axis=0` to indicate that we want to append the row along the vertical axis (i.e. as a new row).

## Adding a Row to an Empty Numpy Array

Adding a row to an empty numpy array is similar to appending a row to an existing array. We can first create the empty array and then use the `numpy.append()` function to add the row. Continuing from the previous example, let's say we want to create an empty 0x3 array of type `int` and add the row `[1,2,3]` to it. We can do the following:

``` python
a = np.zeros((0,3), dtype=int)
row_to_add = np.array([1,2,3])
a = np.append(a, [row_to_add], axis=0)
```

Here, we first create an empty array of shape (0,3) and then append the row `[1,2,3]` to it.
