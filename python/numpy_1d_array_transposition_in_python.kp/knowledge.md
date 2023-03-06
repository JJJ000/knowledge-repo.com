---
title: Rewording rearranging a one-dimensional array in numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `transpose()` method to transpose a 1D NumPy array in Python.
---

**Contents**

[TOC]

### Introduction 
NumPy (Numerical Python) is an open source Python library used for scientific computing, data analysis and manipulation. One of the most used data structures in NumPy is an array. We can transform (transpose) an array in NumPy by changing the shape of the array. 

### Transposing a 1D NumPy array using reshape() function
The transpose of a 1D array in NumPy is the same array itself. Therefore, we need to reshape the 1D array into a 2D array with dimensions 1xN or Nx1 to transpose it. 

``` python
import numpy as np

a = np.array([1, 2, 3, 4, 5])  # create a 1D array

a_T = a.reshape(-1, 1)  # reshape the 1D array into a 2D array with dimensions 5x1

print("Original array:\n", a)
print("Transpose of the array:\n", a_T)
```
Output:
```
Original array:
 [1 2 3 4 5]
Transpose of the array:
 [[1]
 [2]
 [3]
 [4]
 [5]]
```
### Transposing a 1D NumPy array using the T attribute
NumPy arrays have an attribute T, which returns the transpose of the array. For a 1D array, the T attribute has no effect as the transpose of a 1D array is the same array itself. 

``` python
import numpy as np

a = np.array([1, 2, 3, 4, 5])  # create a 1D array

a_T = a.T  # using the T attribute

print("Original array:\n", a)
print("Transpose of the array:\n", a_T)
```
Output:
```
Original array:
 [1 2 3 4 5]
Transpose of the array:
 [1 2 3 4 5]
```

### Transposing a 1D NumPy array using None indexing
We can use None indexing to add a new axis to a 1D array, which makes it a 2D column array. Then, we can transpose the array using the T attribute or swapaxes() function.

``` python
import numpy as np

a = np.array([1, 2, 3, 4, 5])  # create a 1D array

a_col = a[:, None]  # adding a new axis and converting to column array

a_T = a_col.T  # using the T attribute

print("Original array:\n", a)
print("Transpose of the array:\n", a_T)
```
Output:
```
Original array:
 [1 2 3 4 5]
Transpose of the array:
 [[1 2 3 4 5]]
``` 

We can also use the swapaxes() function to transpose the array:

``` python
a_T = a_col.swapaxes(0, 1)  # using the swapaxes() function

print("Original array:\n", a)
print("Transpose of the array:\n", a_T)
```
Output:
```
Original array:
 [1 2 3 4 5]
Transpose of the array:
 [[1 2 3 4 5]]
```

### Conclusion
In this tutorial, we explored different ways to transpose a 1D NumPy array in Python. We can reshape a 1D array to a column or row array to make it a 2D array and then transpose it using the T attribute or the swapaxes() function. We can also use None indexing to add a new axis to a 1D array and then transpose it using the T attribute or the swapaxes() function.
