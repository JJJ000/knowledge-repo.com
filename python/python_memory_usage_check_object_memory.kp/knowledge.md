---
title: Determine the amount of memory being utilized by an object in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use the sys.getsizeof() function to find out how much memory is being used by an object in Python.
---

**Contents**

[TOC]

## Using the `sys` module

One way to find out how much memory is being used by an object in Python is to use the `sys` module. The `getsizeof()` function in the `sys` module returns the size of an object in bytes. For example:

```python
import sys

my_list = [1, 2, 3]
print(sys.getsizeof(my_list))
```

This will output something like `80` (depending on the version and implementation of Python you are using), which is the number of bytes used by the `my_list` object in memory.


## Using the `pympler` module

Another way to find out how much memory is being used by an object in Python is to use the `pympler` module. This module provides a set of tools for working with Python memory usage.

```python
from pympler import asizeof

my_dict = {"key": "value"}
print(asizeof.asizeof(my_dict))
```

This will output something like `232` (depending on the version and implementation of Python you are using), which is the number of bytes used by the `my_dict` object in memory.


## Using `tracemalloc`

Another way to find out how much memory is being used by an object in Python is to use the `tracemalloc` module. This module provides a way to trace memory allocations in Python.

```python
import tracemalloc

tracemalloc.start()

my_string = "hello world"
print(tracemalloc.get_traced_memory()[0])

tracemalloc.stop()
```

This will output something like `57` (depending on the version and implementation of Python you are using), which is the number of bytes used by the `my_string` object in memory.


## Summary

In summary, there are several ways to find out how much memory is being used by an object in Python. The `sys.getsizeof()` function can be used to get the size of an object in bytes. The `pympler.asizeof()` function can be used to get a more accurate measurement of memory usage, taking into account object overhead and other factors. The `tracemalloc` module can be used to trace memory allocations and see how much memory is being used by specific objects.
