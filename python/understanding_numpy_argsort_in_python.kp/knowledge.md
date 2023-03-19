---
title: What does numpy argsort entail?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Numpy argsort returns the indices that would sort an array in ascending order.
---

**Contents**

[TOC]

Introduction

In Python, Numpy is a package that is commonly used for scientific computing. One of its useful functions is argsort which is used to sort an array and return the indices that would sort the array. 

Section 1: Sorting an Array

Before diving into argsort, it is important to understand how to sort an array. In Numpy, one can easily sort an array using the sort() method. When sorting an array using this method, elements are rearranged in ascending order by default. For instance:

```
import numpy as np

x = np.array([3, 1, 4, 2, 6, 5])
np.sort(x)
```
This will result in an array [1, 2, 3, 4, 5, 6] being printed.  

Section 2: Using Argsort

Numpy argsort is used when we need to know the position of each element if the array was sorted. For instance, if we have an array:

```
x = np.array([3, 1, 4, 2, 6, 5])
```

we can use argsort to get the indices that would sort this array using:

```
np.argsort(x)
```

This will return an array [1, 3, 0, 2, 5, 4] being printed which shows the positions of the sorted elements.

Section 3: Using Argsort to Sort Along an Axis

Often times, we may want to sort along a particular axis of a multidimensional array. This is when argsort really shines. For instance:

```
x = np.array([[3, 2], [1, 4]])
np.argsort(x, axis=0)
```

This will result in an array [[1, 0], [0, 1]] being printed since the first column would be sorted as [1, 3] and the second column sorted as [2, 4]. Therefore, the first column would contain indices [1, 0] and the second column indices [0, 1]. 

Section 4: Conclusion

In conclusion, Numpy argsort is a useful function used to sort Numpy arrays and return the indices that would sort the array. It can also be used to sort along an axis of a multidimensional array.
