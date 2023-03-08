---
title: Enumerating the elements of an array in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To count the number of elements in a Python array, use the len() function.
---

**Contents**

[TOC]

## Introduction

Counting the number of elements in an array is one of the most simple tasks that Python programmers may face in their projects. In this tutorial, we'll take a look at some of the possible ways to count elements in an array in Python.


## Using the len() function

The `len()` function returns the number of items in an iterable object. As arrays are iterable objects in Python, we can use the `len()` function to count the number of elements in an array as well.

```python
my_array = [1, 2, 3, 4, 5]
array_length = len(my_array)

print("The length of the array is:", array_length)
```


## Using a loop

We can also use a loop to iterate over the elements of an array and count them. Here's an example:

```python
my_array = [1, 2, 3, 4, 5]
count = 0

for element in my_array:
    count += 1

print("The length of the array is:", count)
```


## Using the numpy library

If you're working with arrays in Python, chances are that you've already come across the numpy library. The numpy library provides a lot of useful functions for working with arrays, including one for counting the number of elements in an array.

```python
import numpy as np

my_array = np.array([1, 2, 3, 4, 5])
array_length = np.size(my_array)

print("The length of the array is:", array_length)
```


## Conclusion

These are some of the possible ways to count elements in an array in Python. Depending on your needs and preferences, you may choose one method over the others. However, the `len()` function is probably the most commonly used one, as it is simple and efficient.
