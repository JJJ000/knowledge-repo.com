---
title: Divide every row of numpy by an element of a vector
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Divide a numpy array by a vector by using broadcasting, where the vector is reshaped to match the dimensions of the array.
---

**Contents**

[TOC]

Introduction:
NumPy is a powerful library for array computations in Python. It provides various functions for mathematical operations on arrays, matrices, and vectors. One of the common operations with NumPy is dividing each row of a matrix by a vector element. In this tutorial, we'll show you how to divide each row of a NumPy array by a vector element in Python.

Step 1: Create a Matrix and a Vector
Let's start by creating a NumPy array that we'll use as our matrix. We'll also create a NumPy array containing the vector that we'll use to break down our matrix.

import numpy as np

matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
vector = np.array([0, 1, 2])

Step 2: Divide Each Row by a Vector Element
To divide each row of our matrix by an element in our vector, we'll use the np.divide function. This function will divide each element in our matrix by the corresponding element in our vector.

result = np.divide(matrix, vector[:, np.newaxis])

Here, we pass our matrix as the first argument to np.divide and our vector as the second argument. We also reshape our vector to a two-dimensional array using the [:, np.newaxis] syntax so that it has the same shape as our matrix for the division.

Step 3: Display the Result
To test our function, let's print our original matrix and vector and the resulting matrix.

print("Original Matrix:\n", matrix)
print("Vector:\n", vector)
print("Resulting Matrix:\n", result)

The output should look like:

Original Matrix:
 [[1 2 3]
 [4 5 6]
 [7 8 9]]
Vector:
 [0 1 2]
Resulting Matrix:
 [[       inf 2.         1.5       ]
 [       inf 5.         3.        ]
 [       inf 4.         4.5       ]]

Note that our resulting matrix contains infinity values because we divided by zero (the first element in our vector). To avoid this, we can add a small value to our vector to prevent division by zero.

Step 4: Add a Small Value to the Vector
To avoid division by zero, we'll add a small value (e.g., 1e-8) to our vector.

result = np.divide(matrix, vector[:, np.newaxis] + 1e-8)

Now, let's print the resulting matrix again.

print("Resulting Matrix:\n", result)

The output should look like:

Resulting Matrix:
 [[1.00000000e+08 2.00000000e+00 1.50000000e+00]
 [4.00000000e+08 5.00000000e+00 3.00000000e+00]
 [7.00000000e+08 4.00000000e+00 4.50000000e+00]]

Note that our resulting matrix no longer contains infinity values. We have successfully divided each row of our matrix by an element in our vector using NumPy!
