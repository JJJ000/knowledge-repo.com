---
title: Substitute all items in a Python numpy array that exceed a certain threshold
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the NumPy function np.where() to replace all elements that are greater than the specified value with a new value.
---

**Contents**

[TOC]

## Introduction

In some cases, we may need to replace all the elements of a NumPy array that are greater than some specific value with another value. This can be done easily using NumPy built-in functions.

In this tutorial, we'll show you how to replace all the elements of a NumPy array that are greater than a specific value in two different ways.

## Method 1: np.where()

One of the easiest ways to replace the elements of a NumPy array is by using the `np.where()` function. The `np.where()` function takes three arguments: a boolean expression, a value to replace True elements, and a value to replace False elements. 

Here's how to use the `np.where()` function to replace all elements greater than a specific value with another value:

```python
import numpy as np

# Create a NumPy array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# Replace all elements greater than 5 with 0
new_arr = np.where(arr > 5, 0, arr)

print(new_arr)
```

Output:

```
[1 2 3 4 5 0 0 0 0 0]
```

In this example, we replaced all elements greater than 5 with 0.

## Method 2: boolean indexing

Another way to replace all elements greater than a specific value is by using boolean indexing. This method involves creating a boolean mask for elements that meet the condition and assigning a new value to those elements.

Here's how to use boolean indexing to replace all elements greater than a specific value:

```python
import numpy as np

# Create a NumPy array
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# Create a boolean mask based on the condition
mask = arr > 5

# Replace all elements that meet the condition with 0
arr[mask] = 0

print(arr)
```

Output:

```
[1 2 3 4 5 0 0 0 0 0]
```

In this example, we created a boolean mask based on the condition `arr > 5` and assigned `0` to all elements that met the condition.

## Conclusion

In this tutorial, we showed you how to replace all elements of a NumPy array that are greater than a specific value using two different methods: `np.where()` and boolean indexing. These methods are simple and efficient in achieving this task.
