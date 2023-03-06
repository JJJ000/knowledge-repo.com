---
title: In python, initialize a list with a certain capacity
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python, you can create a list with initial capacity by using a list comprehension or by calling the list constructor with an iterable that has a defined size.
---

**Contents**

[TOC]

## Introduction

In Python, we can create a list with an initial capacity. This is useful when we know the approximate size of the list beforehand and want to save memory by allocating space for the list elements in advance. In this article, we will explore different ways of creating a list with an initial capacity.

## Using list comprehension

One way of creating a list with an initial capacity is by using list comprehension. We can create a list with n elements by using the following syntax:

```python
n = 10
my_list = [None] * n
```

In this example, we create a list with 10 `None` elements. We can replace `None` with any other value as per our requirement.

## Using the `array` module

Another way of creating a list with an initial capacity is by using the `array` module from Python's standard library. The `array` module provides a fast and memory-efficient alternative to Python's built-in `list` type.

We can create an array of size n filled with default values by using the following syntax:
```python
from array import array
n = 10
my_array = array('i', [0] * n)
```

In this example, we create an array of size 10 filled with `0` as the default value.

## Using the `numpy` library

If we need to create a list with a large initial capacity or perform mathematical operations on the elements of the list, we can use the popular `numpy` library. 

We can create a `numpy` array of size n filled with default values by using the following syntax:
```python
import numpy as np
n = 10
my_array = np.empty(n, dtype=int)
```

In this example, we create an array of size 10 filled with default value of `0`.

## Conclusion

In this article, we explored different ways of creating a list with an initial capacity in Python. We can use list comprehension, the `array` module or the `numpy` library depending on our use case. By creating a list with an initial capacity, we can save memory and improve the performance of our Python programs.
