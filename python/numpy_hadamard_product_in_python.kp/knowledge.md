---
title: What is the method to achieve hadamard product (element-wise matrix multiplication) using numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the * symbol operator between two matrices or arrays, e.g., C = A * B to perform element-wise matrix multiplication (Hadamard product) in numpy.
---

**Contents**

[TOC]

# Introduction

Matrix multiplication is a common operation when working with matrices, but there are cases where we may want to perform element-wise multiplication. This operation is known as the Hadamard product. In this article, we will discuss how to perform the Hadamard product in Python using the numpy library.

# Importing numpy

Before we start performing the Hadamard product, we need to import the numpy library. We can do this by running the following code:

``` python
import numpy as np
```

This will import the numpy library and we can use it to create and manipulate arrays.

# Performing the Hadamard product

To perform the Hadamard product, we need to have two matrices of the same shape. We can then multiply each element of one matrix with the corresponding element of the other matrix. We can do this using the '*' operator in numpy.

For example:

``` python
a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])
c = a * b
```

This will create two matrices a and b and then multiply them element-wise to create a new matrix c.

# Example

Let's say we have two matrices a and b as given below:

``` python
a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])
```

We can perform the Hadamard product using the following code:

``` python
c = a * b
```

This will create a new matrix c that is the result of the Hadamard product of a and b. The resulting matrix will be:

``` python
[[ 5, 12],
 [21, 32]]
```

This is the element-wise multiplication of the two matrices.
