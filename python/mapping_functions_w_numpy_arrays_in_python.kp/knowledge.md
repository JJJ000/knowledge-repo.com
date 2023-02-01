---
title: What is the quickest way to apply a function to a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The most efficient way to map a function over a numpy array is to use the numpy.vectorize() function.
---

**Contents**

[TOC]

**1. Using Numpy Vectorize** 
Numpy vectorize is a powerful tool that allows you to apply a function to a numpy array quickly and efficiently. It works by taking the input array and applying the function element-wise, meaning that the output of the function is the same shape as the input array. To use it, you simply need to pass the function you want to apply as the first argument and the array you want to apply it to as the second argument. For example: 

```
import numpy as np

def my_func(x):
    return x**2

arr = np.array([1, 2, 3])

# Apply my_func to arr
result = np.vectorize(my_func)(arr)

# Print result
print(result)
```

**2. Using Numpy Apply_Along_Axis** 
Numpy apply_along_axis is a powerful function that allows you to apply a function to a numpy array along a particular axis. This is useful when you have an array of different shapes and you want to apply the same function to each element. To use it, you need to pass the function you want to apply as the first argument, the axis you want to apply it along as the second argument, and the array you want to apply it to as the third argument. For example: 

```
import numpy as np

def my_func(x):
    return x**2

arr = np.array([[1, 2, 3], [4, 5, 6]])

# Apply my_func to arr along axis 0
result = np.apply_along_axis(my_func, 0, arr)

# Print result
print(result)
```

**3. Using Numpy Fromiter** 
Numpy fromiter is a powerful function that allows you to apply a function to a numpy array using an iterator. This is useful when you have an iterator that generates a sequence of values and you want to apply a function to each of the values. To use it, you need to pass the function you want to apply as the first argument, the iterator as the second argument, and the shape of the output array as the third argument. For example: 

```
import numpy as np

def my_func(x):
    return x**2

it = iter([1, 2, 3])

# Apply my_func to it
result = np.fromiter(it, dtype=float, count=-1).reshape(3,1)

# Print result
print(result)
```

**4. Using Numpy Ufuncs** 
Numpy ufuncs are a powerful set of functions that allow you to apply a function to a numpy array quickly and efficiently. They work by taking the input array and applying the function element-wise, meaning that the output of the function is the same shape as the input array. To use them, you simply need to pass the function you want to apply as the first argument and the array you want to apply it to as the second argument. For example: 

```
import numpy as np

arr = np.array([1, 2, 3])

# Apply np.square to arr
result = np.square(arr)

# Print result
print(result)
```
