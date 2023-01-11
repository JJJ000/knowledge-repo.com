---
title: What is the process for converting a string to a float or int?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Use the `float()` or `int()` function to parse a string to a `float` or `int` in Python.
---

**Contents**

[TOC]

### Using the `float()` Function
The `float()` function can be used to parse a string to a float in Python. This function takes a single argument, which is the string to be converted, and returns the float value.

Example:
```python
num_str = "3.14"
num_float = float(num_str)
print(num_float)
# Output: 3.14
```

### Using the `int()` Function
The `int()` function can be used to parse a string to an int in Python. This function takes a single argument, which is the string to be converted, and returns the int value.

Example:
```python
num_str = "42"
num_int = int(num_str)
print(num_int)
# Output: 42
```

### Using `str.split()`
The `str.split()` method can be used to parse a string to a list of strings. This method takes a single argument, which is the delimiter to be used to split the string, and returns a list of strings.

Example:
```python
num_str = "3,14"
num_list = num_str.split(",")
print(num_list)
# Output: ['3', '14']
```

### Using `str.replace()`
The `str.replace()` method can be used to parse a string to a string with a different value. This method takes two arguments, the string to be replaced and the string to replace it with, and returns a new string.

Example:
```python
num_str = "3,14"
num_str = num_str.replace(",", ".")
print(num_str)
# Output: 3.14
```
