---
title: One way to make only certain dimensions of a numpy array flat is by doing what?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `numpy.reshape()` method on the array while specifying the dimensions that need to be flattened using `-1` as the dimension value.
---

**Contents**

[TOC]

## 1. Introduction

In numpy arrays, we can flatten an array to convert it into a one-dimensional (1D) array. However, sometimes we may want to flatten only certain dimensions of an array while keeping the others intact. In this tutorial, we will discuss different ways to flatten only some dimensions of a numpy array in Python.

## 2. Flattening specific dimensions of a numpy array

We can use the numpy's `.reshape()` method to reshape the array dimensions. To flatten a specific dimension of a numpy array, we can set the corresponding dimension size to `-1`. This will automatically calculate the size of that dimension based on the other dimensions, effectively flattening it.

Let's consider a 3-dimensional numpy array of size (2,3,4). To flatten the second dimension, we can set the second dimension size to `-1` in the `.reshape()` method as shown below:

```python
import numpy as np

# create a 3D numpy array of size (2,3,4)
arr_3d = np.arange(24).reshape(2,3,4)
print(arr_3d)
# Output: 
# array([[[ 0,  1,  2,  3],
#         [ 4,  5,  6,  7],
#         [ 8,  9, 10, 11]],
#
#        [[12, 13, 14, 15],
#         [16, 17, 18, 19],
#         [20, 21, 22, 23]]])

# flatten the 2nd dimension
arr_2d = arr_3d.reshape(2, -1, 4)
print(arr_2d)
# Output:
# array([[[ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11]],
#        [[12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23]]])
```

Here, we set the second dimension size to `-1`, and the `.reshape()` method automatically calculates the number of elements to be 1x12. The remaining dimensions (2,4) are preserved, and the array is "unflattened".

## 3. Flattening multiple dimensions of a numpy array

We can extend the above approach to flatten multiple dimensions of a numpy array. We can set multiple dimension sizes to `-1` in the `.reshape()` method. The order in which we set the size `-1` will determine the order of the flattened dimensions.

Let's consider a 3-dimensional numpy array of size (2,3,4). To flatten the first and third dimensions, we can set the sizes to `-1` in the `.reshape()` method as shown below:

```python
import numpy as np

# create a 3D numpy array of size (2,3,4)
arr_3d = np.arange(24).reshape(2,3,4)
print(arr_3d)
# Output: 
# array([[[ 0,  1,  2,  3],
#         [ 4,  5,  6,  7],
#         [ 8,  9, 10, 11]],
#
#        [[12, 13, 14, 15],
#         [16, 17, 18, 19],
#         [20, 21, 22, 23]]])

# flatten the 1st and 3rd dimension
arr_2d = arr_3d.reshape(-1, 3*4)
print(arr_2d)
# Output:
# array([[ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9, 10, 11],
#        [12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23]])
```

Here, we set the first and third dimension sizes to `-1`, and the `.reshape()` method automatically calculates the number of elements to be 2x(3x4)=2x12. The result is a 2D array of size (2,12).


## 4. Conclusion

In numpy arrays, we can flatten only some dimensions of an array while keeping the others intact, using the `.reshape()` method. We can set the size of the dimensions we want to flatten to `-1`, and the `.reshape()` method automatically calculates the number of elements for the flattened dimensions. This way, we can transform multi-dimensional arrays into 1D or 2D arrays as per our needs for further processing.
