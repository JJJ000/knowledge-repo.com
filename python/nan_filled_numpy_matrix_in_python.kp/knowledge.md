---
title: Generate a numpy matrix that contains nan values throughout
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `numpy.full` function with the parameter `fill\_value=np.NaN` to create a matrix filled with NaNs.
---

**Contents**

[TOC]

## Introduction
In this task, we need to create a numpy matrix filled with NaNs in Python. Nano is short for Not a Number, which is a special floating point value that represents undefined or unrepresentable values. It's commonly used in arrays to represent missing or incomplete data.

## numpy.nan
The numpy library provides a special value for NaN which can be accessed using the `numpy.nan` attribute. This value can be used as a placeholder for missing data in numpy arrays.

## numpy.full
The numpy library provides a `full` function that can be used to create an array of a given shape and data type, filled with a specified value. We can use this function to create a matrix filled with NaNs.

```python
import numpy as np

# create a 2x3 matrix filled with NaNs
nan_matrix = np.full((2, 3), np.nan)

print(nan_matrix)
```

Output:
```
[[ nan  nan  nan]
 [ nan  nan  nan]]
```

The `full` function takes two arguments:
- The shape of the array (in this case, `(2, 3)` to create a 2x3 matrix)
- The value to fill the array with (in this case, `np.nan` to fill it with NaNs)

## Conclusion
In this task, we learned how to create a numpy matrix filled with NaNs in Python using the `numpy.full` function. We can use this matrix as a placeholder for missing or incomplete data in our numpy arrays.
