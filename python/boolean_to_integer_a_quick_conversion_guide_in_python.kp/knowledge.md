---
title: What are the steps to transform a boolean array into an integer array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: One possible way to convert a boolean array to an int array in Python is to use the numpy library and its astype() method arr.astype(int).
---

**Contents**

[TOC]

1. Explanation of the problem

In Python, boolean arrays contain elements that are of type `bool`, which has two values: `True` and `False`. However, there are situations where we need to convert boolean arrays to integer arrays, where the `True` and `False` values are converted to `1` and `0`, respectively. This can be necessary, for example, when we need to perform mathematical operations on the elements of the array, which require numerical values. In this tutorial, we will discuss how to convert a boolean array to an int array in Python.


2. Using numpy library to convert boolean array to int array

One of the easiest ways to convert a boolean array to an int array in Python is to use the `numpy` library. This library provides the `astype()` method that allows us to convert one data type to another. To convert a boolean array to an int array, we can use the following code:

```python
import numpy as np

bool_array = np.array([True, False, True])
int_array = bool_array.astype(int)

print(int_array)
```

Output:
```python
[1 0 1]
```


3. Using list comprehension to convert boolean array to int array

Another way to convert a boolean array to an int array in Python is to use list comprehension. We can iterate over the boolean array and convert each element to an integer using the `int()` function. Then, we can store the integers in a new array. Here's an example:

```python
bool_array = [True, False, True]
int_array = [int(x) for x in bool_array]

print(int_array)
```

Output:
```python
[1, 0, 1]
```


4. Using map() and lambda functions to convert boolean array to int array

We can also use the `map()` and `lambda` functions to convert a boolean array to an int array in Python. The `map()` function applies a function to every element of an iterable, and the `lambda` functions are used to create small anonymous functions. Here's an example:

```python
bool_array = [True, False, True]
int_array = list(map(lambda x: int(x), bool_array))

print(int_array)
```

Output:
```python
[1, 0, 1]
```
