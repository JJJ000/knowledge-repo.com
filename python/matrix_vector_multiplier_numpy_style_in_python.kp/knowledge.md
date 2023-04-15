---
title: The multiplication of a vector with a matrix using numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, numpy matrix vector multiplication can be performed using the dot product function, np.dot(matrix, vector).
---

**Contents**

[TOC]

Introduction to NumPy Matrix Vector Multiplication

NumPy is a Python library used for scientific computing. It provides support for large, multidimensional arrays and matrices, along with a vast collection of mathematical functions to operate on these arrays. One of the key advantages of NumPy is its performance, which is significantly better than Python's built-in list operation.

Matrix vector multiplication is a fundamental operation in linear algebra. It is performed by multiplying a matrix with a vector to produce a new vector. In this article, we'll explore how to perform matrix vector multiplication in Python using NumPy.

Creating a NumPy Matrix and Vector

To perform matrix vector multiplication in NumPy, we first need to create a matrix and a vector. We can create a matrix using the NumPy's `array()` function, which takes a list of lists as an argument. Each list represents a row in the matrix.

```python
import numpy as np

# create a 2x2 matrix
matrix = np.array([[1, 2], [3, 4]])

# create a vector
vector = np.array([5, 6])
```

Matrix Vector Multiplication in NumPy

Once we have the matrix and vector, we can perform matrix vector multiplication using the `dot()` function in NumPy. The `dot()` function takes two arguments - the matrix and the vector - and returns a new vector.

```python
# perform matrix vector multiplication
result = np.dot(matrix, vector)

# print the result
print(result)
```

Output:
```
[17 39]
```

As we can see from the output, the result of matrix vector multiplication is a new vector with the same number of rows as the matrix.

Alternatively, we can also use the `@` operator to perform matrix vector multiplication, which was introduced in Python 3.5.

```python
# perform matrix vector multiplication using @ operator
result = matrix @ vector

# print the result
print(result)
```

Output:
```
[17 39]
```

Conclusion

In this article, we explored how to perform matrix vector multiplication in Python using NumPy. We started by creating a NumPy matrix and vector using the `array()` function. We then used the `dot()` function to perform matrix vector multiplication and the `@` operator as an alternative. NumPy's performance and mathematical functions make it an essential library for scientific computing in Python.
