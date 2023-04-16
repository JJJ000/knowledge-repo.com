---
title: What is the most efficient way to find the indices of the n largest elements in a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use np.argpartition to get the indices of the N maximum values in a NumPy array.
---

**Contents**

[TOC]

### Using np.argpartition

The `np.argpartition` function can be used to quickly find the indices of the N maximum values in a NumPy array. It is a faster alternative to `np.argsort` which is more commonly used.

### Syntax

The syntax for `np.argpartition` is as follows:

`np.argpartition(array, kth, axis=-1, kind='introselect', order=None)`

where:

- `array` is the NumPy array
- `kth` is the index of the element that will be used to partition the array
- `axis` is the axis along which the array will be partitioned
- `kind` is the sorting algorithm used to partition the array
- `order` is an optional argument that specifies the order of the elements in the array

### Example

Let's say we have a NumPy array called `arr` and we want to find the indices of the 3 maximum values. We can use `np.argpartition` as follows:

```
indices = np.argpartition(arr, -3, axis=-1, kind='introselect')[-3:]
```

This will return an array of the indices of the 3 maximum values in `arr`.
