---
title: Divide a Python list into several sub-lists, that is, smaller lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use list comprehension with slicing to split a Python list into smaller sublists.
---

**Contents**

[TOC]

## Introduction
Python lists are data structures that can store multiple values. Sometimes, it's useful to split a list into smaller sublists. This can be done in several ways, depending on the specific requirements. In this article, we'll explore some of the ways to split a list in Python.

## Using list comprehension
One way to split a list into sublists is by using list comprehension. This approach is suitable when we have a fixed number of sublists we want to create. Here's an example:

```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
n = 3

sublists = [my_list[i:i+n] for i in range(0, len(my_list), n)]
print(sublists)
```

In this example, we have a list `my_list` with nine elements. We want to split this list into three sublists, each with three elements. We define a variable `n` as the number of elements in each sublist. 

We then use list comprehension to create the sublists. The expression `my_list[i:i+n]` creates a sublist of `my_list` starting at index `i` and ending at index `i+n-1`. The loop iterates over the indices of `my_list` in steps of `n`, so we get three sublists `[1, 2, 3]`, `[4, 5, 6]`, and `[7, 8, 9]`.

## Using numpy
Another way to split a list into sublists is by using the numpy library. This approach is suitable when we want to split a list into sublists of equal size. Here's an example:

```python
import numpy as np

my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
n = 3

sublists = np.array(my_list).reshape(-1, n).tolist()
print(sublists)
```

In this example, we use the numpy library to create sublists. First, we convert the list `my_list` into a numpy array by calling `np.array(my_list)`. We then call the `reshape()` function to reshape the array into a two-dimensional array where each row has `n` elements. 

The `reshape()` function uses the argument `-1` to infer the number of rows needed to accommodate all elements in the array. Finally, we convert the two-dimensional numpy array back to a list using the `tolist()` method to get the sublists `[1, 2, 3]`, `[4, 5, 6]`, and `[7, 8, 9]`.

## Using chunked
Another way to split a list into sublists is by using the `chunked` function from the `more_itertools` library. This approach is useful when we want to split a list into sublists of equal size, but we don't want to use numpy. Here's an example:

```python
from more_itertools import chunked

my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
n = 3

sublists = list(chunked(my_list, n))
print(sublists)
```

In this example, we use the `chunked` function to split the list `my_list` into sublists of equal size. The first argument to `chunked()` is the iterable we want to split, and the second argument is the size of each chunk.

The `chunked()` function returns a generator, so we convert it to a list using `list(chunked(my_list, n))`. This returns the sublists `[1, 2, 3]`, `[4, 5, 6]`, and `[7, 8, 9]`.

## Conclusion
In this article, we explored some of the ways to split a list into sublists in Python. We showed how to use list comprehension, numpy, and the `chunked` function from the `more_itertools` library. Depending on the specific requirements, one of these approaches may be more suitable than others.
