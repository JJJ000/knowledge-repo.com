---
title: Grasping the functionality of numpy's einsum
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: NumPy`s einsum is a powerful tool for performing array operations and broadcasting, allowing for concise and efficient expression of array operations.
---

**Contents**

[TOC]

# Section 1: Overview

NumPy's einsum is a function that allows for efficient multidimensional array operations. It is a powerful tool for manipulating large arrays of data and can be used to calculate inner products, outer products, and other operations on arrays. It is particularly useful for linear algebra operations, such as matrix multiplication and vector dot products.

# Section 2: Syntax

The syntax of einsum is relatively simple. It takes two arguments, a string of subscripts and an array of arrays. The subscripts are used to specify the dimensions of the arrays and the operations to be performed. The array of arrays is used to provide the data for the operations.

# Section 3: Examples

The following example shows how to use einsum to calculate the inner product of two vectors.

```
import numpy as np

a = np.array([1,2,3])
b = np.array([4,5,6])

np.einsum('i,i', a, b)
```

The output of this example is 32, which is the inner product of the two vectors.

# Section 4: Benefits

The main benefit of einsum is its efficiency. By using subscripts to specify the dimensions and operations, it is able to perform complex operations on large arrays quickly and with minimal memory usage. It is also easy to read and understand, making it a great tool for data scientists and machine learning practitioners.
