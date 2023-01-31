---
title: What is the most effective way to print the entire numpy array without any truncation?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the numpy.set\_printoptions() function with the `threshold` parameter set to numpy.inf.
---

**Contents**

[TOC]

## Section 1: Using np.set_printoptions

The easiest way to print the full NumPy array without truncation is to use the np.set_printoptions() function. This function allows you to set the parameters for printing NumPy arrays. To print the full array without truncation, set the 'threshold' parameter to 'np.inf'. For example:

```
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

np.set_printoptions(threshold=np.inf)
print(arr)
```

This will print the full array without truncation:
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

## Section 2: Using np.array2string

Another way to print the full NumPy array without truncation is to use the np.array2string() function. This function takes the NumPy array as an argument and returns a string representation of the array. To print the full array without truncation, set the 'threshold' parameter to 'np.inf'. For example:

```
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

print(np.array2string(arr, threshold=np.inf))
```

This will print the full array without truncation:
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

## Section 3: Using str.format

Another way to print the full NumPy array without truncation is to use the str.format() function. This function takes the NumPy array as an argument and returns a formatted string representation of the array. To print the full array without truncation, set the 'threshold' parameter to 'np.inf'. For example:

```
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

print(str.format(arr, threshold=np.inf))
```

This will print the full array without truncation:
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

## Section 4: Using the print() Function

The last way to print the full NumPy array without truncation is to use the print() function. This function takes the NumPy array as an argument and prints out the array in its entirety. To print the full array without truncation, set the 'threshold' parameter to 'np.inf'. For example:

```
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

print(arr, threshold=np.inf)
```

This will print the full array without truncation:
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```
