---
title: Convert a 2d array of floats to a 2d array of integers using numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the numpy.astype() method to convert a 2D float array to a 2D int array in NumPy.
---

**Contents**

[TOC]

#### Using np.array.astype()

The `astype()` method of the `np.array` class can be used to convert a 2D float array to a 2D int array. This method takes one argument, which is the type to which the array should be converted.

```python
import numpy as np

# Create a 2D float array
float_arr = np.array([[1.2, 2.3, 3.4], [4.5, 5.6, 6.7]])

# Convert to 2D int array
int_arr = float_arr.astype(int)

print(int_arr)

# Output
# [[1 2 3]
#  [4 5 6]]
```

#### Using np.round()

Another method to convert a 2D float array to a 2D int array is to use the `round()` method of the `np.array` class. This method takes one argument, which is the number of decimal places to which the array should be rounded.

```python
import numpy as np

# Create a 2D float array
float_arr = np.array([[1.2, 2.3, 3.4], [4.5, 5.6, 6.7]])

# Convert to 2D int array
int_arr = np.round(float_arr).astype(int)

print(int_arr)

# Output
# [[1 2 3]
#  [4 6 7]]
```

#### Using np.floor()

The `floor()` method of the `np.array` class can also be used to convert a 2D float array to a 2D int array. This method takes one argument, which is the number of decimal places to which the array should be rounded down.

```python
import numpy as np

# Create a 2D float array
float_arr = np.array([[1.2, 2.3, 3.4], [4.5, 5.6, 6.7]])

# Convert to 2D int array
int_arr = np.floor(float_arr).astype(int)

print(int_arr)

# Output
# [[1 2 3]
#  [4 5 6]]
```

#### Using np.ceil()

The `ceil()` method of the `np.array` class can also be used to convert a 2D float array to a 2D int array. This method takes one argument, which is the number of decimal places to which the array should be rounded up.

```python
import numpy as np

# Create a 2D float array
float_arr = np.array([[1.2, 2.3, 3.4], [4.5, 5.6, 6.7]])

# Convert to 2D int array
int_arr = np.ceil(float_arr).astype(int)

print(int_arr)

# Output
# [[2 3 4]
#  [5 6 7]]
```
