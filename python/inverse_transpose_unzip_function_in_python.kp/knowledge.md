---
title: What is the opposite of the zip function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The built-in function zip(*iterables) can be used to unzip an iterable in Python.
---

**Contents**

[TOC]

### Using Itertools
Python's `itertools` module provides the `izip()` function, which is the inverse of the `zip()` function. This function takes an iterable of iterables and returns an iterator of tuples, where the first item in each passed iterable is paired together, and then the second item in each passed iterable are paired together etc.

Example:

```python
from itertools import izip

a = [1, 2, 3]
b = [4, 5, 6]

list(izip(a, b))
# [(1, 4), (2, 5), (3, 6)]
```

### Using Zip
The `zip()` function can be used to unzip a list of tuples. The `zip()` function takes a single iterable containing multiple iterables and returns an iterator of tuples.

Example:

```python
zipped_list = [(1, 4), (2, 5), (3, 6)]

list(zip(*zipped_list))
# [(1, 2, 3), (4, 5, 6)]
```

### Using List Comprehension
List comprehension can also be used to unzip a list of tuples.

Example:

```python
zipped_list = [(1, 4), (2, 5), (3, 6)]

[x for x, y in zipped_list], [y for x, y in zipped_list]
# ([1, 2, 3], [4, 5, 6])
```

### Using Map
The `map()` function can be used to unzip a list of tuples. The `map()` function takes a function and an iterable as arguments and returns an iterator that applies the function to every item of the iterable.

Example:

```python
zipped_list = [(1, 4), (2, 5), (3, 6)]

list(map(lambda x: x[0], zipped_list)), list(map(lambda x: x[1], zipped_list))
# ([1, 2, 3], [4, 5, 6])
```
