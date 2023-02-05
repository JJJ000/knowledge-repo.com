---
title: Creating a numpy array with the same value in each element
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To initialize a NumPy array with identical values, use the np.full() function.
---

**Contents**

[TOC]

# Section 1: Using np.full()

The np.full() function allows us to create a NumPy array with a specified shape and fill it with a given value.

Syntax:
np.full(shape, fill_value, dtype=None, order='C')

Example:

import numpy as np

arr = np.full((3,3), 5)
print(arr)

Output:
[[5 5 5]
 [5 5 5]
 [5 5 5]]

# Section 2: Using np.ones()

The np.ones() function allows us to create a NumPy array with a specified shape and fill it with ones.

Syntax:
np.ones(shape, dtype=None, order='C')

Example:

import numpy as np

arr = np.ones((3,3), dtype=int)
print(arr)

Output:
[[1 1 1]
 [1 1 1]
 [1 1 1]]

# Section 3: Using np.zeros()

The np.zeros() function allows us to create a NumPy array with a specified shape and fill it with zeros.

Syntax:
np.zeros(shape, dtype=None, order='C')

Example:

import numpy as np

arr = np.zeros((3,3), dtype=int)
print(arr)

Output:
[[0 0 0]
 [0 0 0]
 [0 0 0]]

# Section 4: Using np.fill()

The np.fill() function allows us to fill an existing NumPy array with a given value.

Syntax:
np.fill(array, value)

Example:

import numpy as np

arr = np.array([[1,2,3], [4,5,6], [7,8,9]])
np.fill(arr, 5)
print(arr)

Output:
[[5 5 5]
 [5 5 5]
 [5 5 5]]
