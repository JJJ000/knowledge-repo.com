---
title: What is the most efficient way to convert a list of lists into a single list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: To make a flat list out of a list of lists in Python, use the `itertools.chain` method.
---

**Contents**

[TOC]

### Using List Comprehension

One way to make a flat list out of a list of lists is to use list comprehension. This involves using a for loop to iterate through the list of lists and adding each element to a new list.

```python
flat_list = [item for sublist in list_of_lists for item in sublist]
```

### Using itertools.chain

Another way to make a flat list out of a list of lists is to use the itertools.chain function. This function takes an iterable of iterables and returns an iterator of the contents of the iterables. 

```python
import itertools

flat_list = list(itertools.chain(*list_of_lists))
```

### Using sum

A third way to make a flat list out of a list of lists is to use the built-in sum function. This function takes an iterable of iterables and returns the sum of all the elements in the iterables.

```python
flat_list = sum(list_of_lists, [])
```

### Using reduce

A fourth way to make a flat list out of a list of lists is to use the built-in reduce function. This function takes a function and an iterable and applies the function to the elements of the iterable, from left to right, to reduce the iterable to a single value. 

```python
from functools import reduce

flat_list = reduce(lambda x,y: x+y, list_of_lists)
```
