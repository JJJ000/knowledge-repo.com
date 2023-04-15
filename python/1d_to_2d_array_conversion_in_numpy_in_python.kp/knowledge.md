---
title: In numpy, how to transform a 1d array into a 2d array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the reshape() method in NumPy to convert a 1D array to a 2D array.
---

**Contents**

[TOC]

Section 1: Introduction
Numpy is a popular library in Python used for scientific computations. One of its main features is the ability to perform operations on arrays. In this tutorial, we will focus on how to convert a 1D array to a 2D array in numpy in Python.

Section 2: Creating a 1D array
To create a 1D array in numpy, we can use the `numpy.array()` method. We can pass a list of values to this method which will create a 1D array.

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print(arr)
# Output: [1 2 3 4 5]
```

Section 3: Converting a 1D array to a 2D array
To convert a 1D array to a 2D array in numpy, we can use the `numpy.reshape()` method. We can pass the shape of the new array as a tuple to this method.

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
new_arr = arr.reshape((1, 5))
print(new_arr)
# Output: [[1 2 3 4 5]]
```

In this example, we have changed the shape of the array to `(1, 5)` which means we want a 2D array with one row and five columns.

Section 4: Conclusion
In this tutorial, we have learned how to create a 1D array in numpy and how to convert it to a 2D array using the `numpy.reshape()` method. These are important concepts to learn if you want to work with numpy arrays in Python.
