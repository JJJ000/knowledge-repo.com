---
title: How do the flatten and ravel functions in numpy differ?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Flatten returns a copy of the array collapsed into one dimension, while ravel returns a view of the original array with the same data in one dimension.
---

**Contents**

[TOC]

### Flatten
The `flatten()` function in NumPy returns a copy of an array collapsed into one dimension. It is a method of the ndarray object and takes an optional order argument. The default order is ‘C’ which means that the elements are read row-wise, ‘F’ means that the elements are read column-wise, and ‘A’ means that the elements are read in Fortran-like index order. 

### Ravel
The `ravel()` function in NumPy returns a flattened array, but it does not return a copy of the original array. It is also a method of the ndarray object and also takes an optional order argument. It is used to unravel the array into a single-dimensional array. The default order is ‘C’ which means that the elements are read row-wise, ‘F’ means that the elements are read column-wise, and ‘A’ means that the elements are read in Fortran-like index order. 

### Difference
The main difference between `flatten()` and `ravel()` is that `flatten()` returns a copy of the original array collapsed into one dimension while `ravel()` returns a view of the original array collapsed into one dimension. Also, `flatten()` is a method of the ndarray object while `ravel()` is a function.
