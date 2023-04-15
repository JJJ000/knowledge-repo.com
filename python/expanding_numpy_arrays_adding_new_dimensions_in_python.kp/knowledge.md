---
title: Is there a way to incorporate additional dimensions into a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `numpy.newaxis` or `None` keyword to add a new dimension to a Numpy array.
---

**Contents**

[TOC]

### 1. Using np.newaxis

The np.newaxis object can be used to add a new dimension to an existing Numpy array. np.newaxis is just an alias for None, and is used to explicitly specify the new dimension. The new dimension added is typically added at the end of the array. 

Example:

`import numpy as np`

`arr = np.array([1,2,3])`

`arr_new = arr[:,np.newaxis]`

This will create a new array with shape (3,1), as the np.newaxis was added at the end.

### 2. Using np.expand_dims

The np.expand_dims() function can also be used to add new dimensions to an existing Numpy array. It allows us to specify the axis along which we want to expand the dimensions. 

Example:

`import numpy as np`

`arr = np.array([1,2,3])`

`arr_new = np.expand_dims(arr, axis=1)`

This will add a new dimension at axis=1, and create a new array with shape (3,1).

### 3. Using np.reshape

Numpy arrays can be reshaped to add new dimensions. The np.reshape() function can be used for this. The reshaped array must have the same number of elements as the original array. 

Example:

`import numpy as np`

`arr = np.array([1,2,3,4])`

`arr_new = arr.reshape(2,2)`

This will create a new array with shape (2,2) by reshaping the original array. 

### 4. Using np.concatenate

The np.concatenate() function can also be used to add new dimensions to a Numpy array. It is typically used to combine two or more arrays along an axis. If two arrays are concatenated along a new axis, a new dimension is added. 

Example:

`import numpy as np`

`arr1 = np.array([[1,2],[3,4]])`

`arr2 = np.array([[5,6],[7,8]])`

`arr_new = np.concatenate((arr1,arr2), axis=0)`

This will concatenate the two arrays along axis=0 and create a new array with shape (4,2). A new dimension is added along axis=0.
