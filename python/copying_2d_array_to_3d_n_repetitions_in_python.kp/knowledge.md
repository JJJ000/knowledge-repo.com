---
title: What is the process for duplicating a 2d array in n instances within a third dimension?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use numpy`s `tile()` function to create a new 3D array by repeating the 2D array N times along the third dimension.
---

**Contents**

[TOC]

## Creating a 2D array in Python

Before copying a 2D array into a 3D array, we first need to create a 2D array. This can be done using Numpy library in Python.

```python
import numpy as np

arr2d = np.array([[1,2,3], [4,5,6], [7,8,9]])
print(arr2d)
```

Output:
```
array([[1, 2, 3],
       [4, 5, 6],
       [7, 8, 9]])
```
This code creates a 2D array of size 3x3 with values 1 through 9.


## Creating a 3D array in Python

A 3D array can be created by using the `reshape()` function provided by Numpy.

```python
arr3d = np.array([arr2d])
print(arr3d.shape)
```

Output:
```
(1, 3, 3)
```
This code creates a 3D array of size 1x3x3 by using the `arr2d` array which we created earlier.


## Copying a 2D array into a 3rd dimension, N times

To copy a 2D array into a 3D array N times, we can make use of Numpy's `tile()` function. 

```python
arr3d = np.tile(arr2d, (N, 1, 1))
print(arr3d.shape)
```

Output:
```
(N, 3, 3)
```

Here, `N` is the number of times we want to copy the 2D array into a 3rd dimension. The `tile()` function takes the `arr2d` array, along with the dimensions in which we want to extend it, and the number of times we want to do this - `(N, 1, 1)`.

This code will return a 3D array of size N x 3 x 3, with every slice being equal to the `arr2d` 2D array. 

## Conclusion

In this tutorial, we have seen how to create a 2D array in Python using Numpy and then copy it into a 3D array N times. This concept can be used in many applications such as image processing where a single 2D image is copied into a 3D array for further processing.
