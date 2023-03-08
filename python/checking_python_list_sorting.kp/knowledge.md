---
title: What is the pythonic approach to determine if a list is sorted or not?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the built-in function `all` with a comparison operator to check if each element is less than or equal to the next one.
---

**Contents**

[TOC]

## Using the all() and comparison operators:

A straightforward approach to check if a list is sorted is to iterate over the list and check if each element is greater than or equal to the previous one. For this, we can use the comparison operators `>=` along with the built-in `all()` function, which returns True if all elements in an iterable are True.

```python
def is_sorted(lst):
    return all(lst[i] <= lst[i+1] for i in range(len(lst)-1))
```

This function returns True if the list is sorted in non-decreasing order and False otherwise.



## Using the sorted() built-in function:

Another option is to create a sorted copy of the list and compare it with the original list. If both lists are equal, then the original list is sorted. However, this approach requires additional memory to create a new list.

```python
def is_sorted(lst):
    return lst == sorted(lst)
```

This function uses the built-in `sorted()` function, which returns a new sorted list from the elements of the iterable passed as an argument.



## Using the bisect() module:

The `bisect()` module in Python provides functions to insert an element into a sorted list and to find the index where an element should be inserted to maintain the order of the list. We can use this module to check if a list is already sorted.

```python
from bisect import bisect_left

def is_sorted(lst):
    return all(lst[i] <= lst[i+1] for i in range(len(lst)-1)) or all(lst[i] >= lst[i+1] for i in range(len(lst)-1))

def is_sorted_using_bisect(lst):
    return all(bisect_left(lst, lst[i]) <= i for i in range(1, len(lst)))
```

In this implementation, we first check if the list is sorted in non-decreasing order using the `all()` function and comparison operators. If the list is not sorted in non-decreasing order, we check if it is sorted in non-increasing order using the same approach. If both conditions fail, we return False.

Next, we define a new function `is_sorted_using_bisect()` that uses the `bisect_left()` function to check if each element is in the correct order relative to the others. The bisect_left() function returns the index where an element should be inserted to maintain the order of the list. If the index of each element is less than or equal to its original index, we conclude that the list is sorted.



## Using the pairwise() function from the itertools module:

Another alternative to check if a list is sorted is to use the `pairwise()` function from the `itertools` module. This function returns an iterator that generates tuples of adjacent elements from the input iterable. We can use this function to iterate over adjacent pairs of elements and check if each pair is in non-decreasing order.

```python
from itertools import pairwise

def is_sorted(lst):
    return all(a <= b for a, b in pairwise(lst))
```

In this implementation, we use the `all()` function and comparison operators to check if all adjacent pairs of elements in the input list are in non-decreasing order. Each pair of adjacent elements is obtained using the `pairwise()` function from the `itertools` module. If all pairs are in non-decreasing order, the function returns True, indicating that the list is sorted.
