---
title: What is the best way to divide a list into equal parts?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Use the built-in function `zip(*[iter(list)]*n)` to split a list into `n` equal-sized chunks.
---

**Contents**

[TOC]

### Using List Comprehension 

List comprehension is an elegant way to define and create lists based on existing lists. It is a very concise and efficient way to split a list into equally-sized chunks in Python.

The syntax for list comprehension is as follows: 

```python
[expression for item in list]
```

Here is an example of how to use list comprehension to split a list into equally-sized chunks: 

```python
my_list = [1,2,3,4,5,6,7,8,9,10]

chunks = [my_list[i:i+3] for i in range(0, len(my_list), 3)]
```

### Using the zip() Function 

The zip() function in Python is used to map the similar index of multiple containers so that they can be used just using as single entity. It takes iterables (can be zero or more), makes an iterator that aggregates elements based on the iterables passed, and returns an iterator of tuples.

The syntax for the zip() function is as follows: 

```python
zip(*iterables)
```

Here is an example of how to use the zip() function to split a list into equally-sized chunks: 

```python
my_list = [1,2,3,4,5,6,7,8,9,10]

chunks = [list(x) for x in zip(*[iter(my_list)]*3)]
```

### Using the Itertools Module 

The itertools module in Python is a collection of tools for handling iterators. It provides a host of useful functions that work on iterators to produce complex iterators.

The syntax for the itertools module is as follows: 

```python
import itertools
```

Here is an example of how to use the itertools module to split a list into equally-sized chunks: 

```python
my_list = [1,2,3,4,5,6,7,8,9,10]

chunks = list(itertools.zip_longest(*[iter(my_list)] * 3, fillvalue=None))
```

### Using the Numpy Module 

The numpy module in Python is a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.

The syntax for the numpy module is as follows: 

```python
import numpy as np
```

Here is an example of how to use the numpy module to split a list into equally-sized chunks: 

```python
my_list = [1,2,3,4,5,6,7,8,9,10]

chunks = np.array_split(my_list, 3)
```