---
title: What is the method for obtaining the index of the maximum element within a given axis of a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: Use `numpy.argmax(array, axis)` to get the index of the maximum element along the specified axis.
---

**Contents**

[TOC]

# Introduction
In scientific computing with Python, NumPy is one of the most useful packages. It provides a fast, flexible and efficient interface to work with large datasets. In many cases, we need to find the index of the maximum element in a NumPy array along a specific axis. In this tutorial, we will learn how to do this efficiently.

# Example dataset
Let's start by creating a NumPy array with some random data. 

``` python
import numpy as np
np.random.seed(42)
arr = np.random.randint(0, 10, (5, 4, 3))
```

Here, we have created a 3D array (5 x 4 x 3) with random integer values between 0 and 10.

# Using `argmax` method
The `argmax` method in NumPy returns the indices of the maximum values along a specific axis. We can simply use this method along the desired axis to get the index of the maximum element.

``` python
max_index = np.argmax(arr, axis=2)
```

Here, we have used the `argmax` method along the third axis (axis=2) to get the indices of the maximum values. The returned `max_index` array will have the same shape as the input array, except for the last dimension, which will be flattened. 

# Using `where` method
We can also use the `where` method in NumPy along with the `max` method to find the index of the maximum element along a specific axis.

``` python
max_index = np.where(arr == np.max(arr, axis=2)[:,:,np.newaxis])
```

Here, we have first used the `max` method along the third axis (axis=2) to get the maximum value of each 2D slice along that axis. We then compared each element of the input array with this maximum value using the `==` operator to get a boolean array. Finally, we have used the `where` method to get the indices of the `True` elements in the boolean array. 

# Conclusion
In this tutorial, we have learned two methods to get the index of the maximum element in a NumPy array along a specific axis. Depending on the use case, one method may be more suitable than the other.
