---
title: What is the method to determine if a numpy array is empty or not?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `numpy.ndarray.size` method to check whether the size of the array is zero or not.
---

**Contents**

[TOC]

## Checking if a numpy array is empty using size and shape attributes

The `numpy` module provides size and shape attributes of an array which can be used to check if the array is empty or not. If the `size` or the product of the elements of the `shape` attribute is equal to zero, then the array is empty. 

```python
import numpy as np

# Creating an empty numpy array
empty_arr = np.array([])

# Checking if the array is empty
if empty_arr.size == 0:
    print("The array is empty")

if np.prod(empty_arr.shape) == 0:
    print("The array is empty")
```

## Checking if a numpy array is empty using any() method

Another way to check if a numpy array is empty is by using the `numpy.any()` method. If the array is empty, then the method returns False. The method returns True if any element of the array is True.

```python
import numpy as np

# Creating an empty numpy array
empty_arr = np.array([])

# Checking if the array is empty
if not np.any(empty_arr):
    print("The array is empty")
```

## Checking if a numpy array is empty using len() function

We can also use the `len()` function in Python to check if a numpy array is empty or not. If the length of the array is equal to zero, then the array is empty.

```python
import numpy as np

# Creating an empty numpy array
empty_arr = np.array([])

# Checking if the array is empty
if len(empty_arr) == 0:
    print("The array is empty")
```

## Conclusion

In this tutorial, we learned how to check if a numpy array is empty using various methods such as the size and shape attributes, the any() method, and the len() function. Depending on the use case, any of these methods can be used to check if a numpy array is empty or not.
