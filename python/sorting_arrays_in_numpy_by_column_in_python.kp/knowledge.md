---
title: Arranging elements of an array in numpy by column
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: In NumPy, arrays can be sorted by column using the np.sort() function.
---

**Contents**

[TOC]

# Section 1: Using np.sort()

The np.sort() function can be used to sort NumPy arrays by column. The syntax for this function is np.sort(array, axis=0). The ‘axis’ parameter specifies the axis along which the array is sorted. If axis is 0, the array is sorted along its columns. If axis is 1, the array is sorted along its rows.

# Section 2: Example

For example, let's say we have a 3x2 array:

```
arr = [[2, 5],
       [1, 4],
       [3, 6]]
```

We can sort this array by column using np.sort():

```
np.sort(arr, axis=0)

array([[1, 4],
       [2, 5],
       [3, 6]])
```

# Section 3: Sorting in Descending Order

The np.sort() function also has an optional parameter, ‘order’, which can be used to sort the array in descending order. The syntax for this is np.sort(array, axis=0, order=‘descending’).

# Section 4: Example

For example, let's say we have the same 3x2 array as before:

```
arr = [[2, 5],
       [1, 4],
       [3, 6]]
```

We can sort this array in descending order by column using np.sort():

```
np.sort(arr, axis=0, order='descending')

array([[3, 6],
       [2, 5],
       [1, 4]])
```
