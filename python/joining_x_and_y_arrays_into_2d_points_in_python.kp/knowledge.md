---
title: Combining the x and y array points to create a single array of 2d points using the cartesian product method
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use numpy.meshgrid function to get the 2D Cartesian product of two arrays x and y in Python.
---

**Contents**

[TOC]

## Section 1: Explanation of Cartesian product

The Cartesian product of two sets X and Y is the set of all possible ordered pairs (x, y), where x is an element of X and y is an element of Y. In the context of arrays, we can think of the Cartesian product as creating a two-dimensional array whose rows are the ordered pairs of elements from the original arrays. 

## Section 2: Using NumPy to create the Cartesian product

NumPy is a powerful library for scientific computing in Python that includes many functions for working with arrays. One such function is `numpy.meshgrid`, which can generate a Cartesian product of two arrays. 

```python
import numpy as np

x = np.array([1, 2, 3])
y = np.array([4, 5, 6])

X, Y = np.meshgrid(x, y)
points = np.column_stack([X.ravel(), Y.ravel()])
```

The `np.meshgrid` function creates two arrays X and Y whose elements are the Cartesian product of x and y. The `np.column_stack` function takes these two arrays and constructs a new 2D array by stacking them horizontally. Finally, we use the `ravel` function to flatten the arrays into one-dimensional arrays and stack them vertically to get a single 2D array of Cartesian product points.


## Section 3: Using itertools to create the Cartesian product

Another way to generate the Cartesian product of two arrays is to use the `itertools` library, which provides many useful functions for working with combinatorial iterators. One such function is `itertools.product`, which can generate the Cartesian product of two iterables.

```python
import itertools

x = [1, 2, 3]
y = [4, 5, 6]

points = list(itertools.product(x, y))
```

The `itertools.product` function takes two iterable objects and returns an iterator that generates the Cartesian product of their elements. We can use the `list` function to convert this iterator to a list of tuples representing the Cartesian product points.


## Section 4: Conclusion

In this post, we have discussed two methods for generating the Cartesian product of two arrays in Python. The `numpy.meshgrid` function is a powerful and efficient way to create the Cartesian product using NumPy, while the `itertools.product` function is a more general-purpose method that can work with any iterable objects. Depending on the situation, one method may be more appropriate than the other.
