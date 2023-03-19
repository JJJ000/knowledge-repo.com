---
title: Create a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To initialize a numpy array in Python, use the numpy.array() function and pass in a list or tuple of values.
---

**Contents**

[TOC]

## Introduction
NumPy is a fundamental library in Python for numerical computing. It provides a high-performance multidimensional array object, and tools for working with these arrays. In this tutorial, we'll learn how to initialize a numpy array in Python.

## Importing NumPy
The first thing you'll need to do to work with NumPy is import the library. We can do this with the following statement:

```python
import numpy as np
```

## Creating a NumPy Array
There are several ways to create a NumPy array. This includes creating an array from a Python list, creating an array of a certain shape and type filled with zeros, and creating an array of a certain shape and type filled with ones.

### Creating an array from a Python list
To create a NumPy array from a Python list, we can use the `np.array()` function. Here's an example:

```python
import numpy as np

my_list = [1, 2, 3, 4, 5]
my_array = np.array(my_list)

print(my_array)
```

Output:
```
[1 2 3 4 5]
```

### Creating an array filled with zeros
To create an array of a certain shape and type filled with zeros, we can use the `np.zeros()` function. Here's an example:

```python
import numpy as np

my_array = np.zeros((2, 3))

print(my_array)
```

Output:
```
[[0. 0. 0.]
 [0. 0. 0.]]
```

### Creating an array filled with ones
To create an array of a certain shape and type filled with ones, we can use the `np.ones()` function. Here's an example:

```python
import numpy as np

my_array = np.ones((2, 3))

print(my_array)
```

Output:
```
[[1. 1. 1.]
 [1. 1. 1.]]
```

## Conclusion
In this tutorial, we learned how to initialize a NumPy array in Python. We learned how to create an array from a Python list, create an array of a certain shape and type filled with zeros, and create an array of a certain shape and type filled with ones.
