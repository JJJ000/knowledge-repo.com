---
title: Conversion of arrays from nd to 1d
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To convert from ND to 1D arrays in Python, use the ravel() method.
---

**Contents**

[TOC]

Section 1: Introduction

In Python, arrays are important data structures that allow you to store and manipulate a collection of data in a single variable. There are different types of arrays you can use in Python, including ND (N-dimensional) and 1D (one-dimensional) arrays. ND arrays are multidimensional arrays, meaning they can store data in multiple dimensions or axes, while 1D arrays are single-dimensional arrays, meaning they can only store data in a single row or column. In this article, we'll discuss how to convert ND arrays to 1D arrays in Python.

Section 2: Converting ND arrays to 1D arrays

The process of converting ND arrays to 1D arrays in Python involves flattening or reshaping the array. There are different methods you can use to achieve this, including the reshape(), ravel(), and flatten() methods.

Method 1: Using the reshape() method

The reshape() method is a built-in method in NumPy, which is a library in Python that adds support for arrays and matrices. This method allows you to reshape an ND array into a 1D array. Here's an example:

```python
import numpy as np

# Create an ND array
nd_array = np.array([[1, 2], [3, 4]])

# Reshape the ND array to a 1D array
one_d_array = nd_array.reshape(-1)

print("ND array:", nd_array)
print("1D array:", one_d_array)
```

Output:

```
ND array: [[1 2]
 [3 4]]
1D array: [1 2 3 4]
```

In the example above, we imported the NumPy library and created an ND array using the np.array() method. We then used the reshape() method to convert the ND array to a 1D array using the -1 argument, which reshapes the array into a single row or column.

Method 2: Using the ravel() method

The ravel() method is another built-in method in NumPy that allows you to flatten an ND array into a 1D array. Here's an example:

```python
import numpy as np

# Create an ND array
nd_array = np.array([[1, 2], [3, 4]])

# Flatten the ND array to a 1D array
one_d_array = nd_array.ravel()

print("ND array:", nd_array)
print("1D array:", one_d_array)
```

Output:

```
ND array: [[1 2]
 [3 4]]
1D array: [1 2 3 4]
```

In the example above, we created an ND array using the np.array() method and then used the ravel() method to flatten the array into a 1D array.

Method 3: Using the flatten() method

The flatten() method is similar to the ravel() method in that it flattens an ND array into a 1D array. The difference is that the flatten() method always returns a copy of the original array, while ravel() returns a view of the original array whenever possible. Here's an example:

```python
import numpy as np

# Create an ND array
nd_array = np.array([[1, 2], [3, 4]])

# Flatten the ND array to a 1D array
one_d_array = nd_array.flatten()

print("ND array:", nd_array)
print("1D array:", one_d_array)
```

Output:

```
ND array: [[1 2]
 [3 4]]
1D array: [1 2 3 4]
```

In the example above, we used the flatten() method to flatten an ND array into a 1D array.

Section 3: Conclusion

In conclusion, converting ND arrays to 1D arrays in Python is a straightforward process that involves flattening or reshaping the array. There are different methods you can use to achieve this, including the reshape(), ravel(), and flatten() methods. The choice of method depends on your specific use case and whether you need a copy or view of the original array.
