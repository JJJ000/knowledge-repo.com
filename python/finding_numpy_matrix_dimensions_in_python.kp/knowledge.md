---
title: What is the method to determine the length or size of a numpy matrix in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can find the dimensions of a numpy matrix by using the .shape attribute.
---

**Contents**

[TOC]

## Section 1: Introduction
In this section, we will briefly discuss what NumPy is and what it is used for in Python.

NumPy is a Python library used for working with arrays. It also has functions for working in domain of linear algebra, Fourier transform, and matrices. NumPy arrays are faster and more efficient than Python lists. NumPy also allows us to perform mathematical operations on these arrays.

## Section 2: Getting the shape of a NumPy matrix
In this section, we will discuss how to get the shape of a NumPy matrix.

The shape of a NumPy matrix tells you the number of rows and columns it has.

To get the shape of a NumPy matrix, we can use the `.shape` property.

```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr.shape)
```

Output:
```
(2, 3)
```

The above code creates a NumPy matrix of 2 rows and 3 columns and prints its shape using the `.shape` property.


## Section 3: Getting the length of a NumPy matrix
In this section, we will discuss how to get the length of a NumPy matrix, which is the number of elements in the matrix.

To get the length of a NumPy matrix, we can use the `.size` property.

```python
import numpy as np
arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr.size)
```

Output:
```
6
```

The above code creates a NumPy matrix of 2 rows and 3 columns and prints its length using the `.size` property.


## Section 4: Conclusion
In this tutorial, we learned how to get the shape and length of a NumPy matrix using the `.shape` and `.size` properties, respectively. These properties are useful when working with data in NumPy as they help us understand the dimensions and size of the data we are working with.
