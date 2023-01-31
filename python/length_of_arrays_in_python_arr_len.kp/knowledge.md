---
title: What is the most efficient way to determine the length of an array in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: No, the preferred way to get the length of an array in Python is to use the len() function.
---

**Contents**

[TOC]

### No

The preferred way to get the length of an array in Python is to use the `len()` function. The `arr.__len__()` syntax is a special method that is used to get the length of an array, but it is not the preferred way.

### Why not?

The `len()` function is the preferred way to get the length of an array in Python because it is simpler and more efficient than the `arr.__len__()` syntax. The `len()` function is also more versatile, as it can be used to get the length of any iterable object, not just arrays.

### How to use `len()`

The `len()` function is used to get the length of an array in Python by passing the array as an argument to the function. For example:

```python
arr = [1, 2, 3]

arr_length = len(arr)

print(arr_length) # prints 3
```

### Summary

In summary, the preferred way to get the length of an array in Python is to use the `len()` function, rather than the `arr.__len__()` syntax. The `len()` function is simpler and more efficient, and it can be used to get the length of any iterable object.
