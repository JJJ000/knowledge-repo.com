---
title: Rapidly detecting nan in numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the function `numpy.isnan(array)` to check for NaN in a NumPy array.
---

**Contents**

[TOC]

There are a few ways to check for NaN (Not a Number) in NumPy arrays in Python. Some methods are faster than others, depending on the size of the array and the way the code is written. Below are some options and their relative speed:

## Method 1: np.isnan()

The np.isnan() function is the most common way to check for NaN in a NumPy array. It returns a boolean array with the same shape as the input array, where True values indicate NaN and False values indicate non-NaN. This method is efficient and concise. 

Example:

```
import numpy as np

arr = np.array([1, 2, np.nan, 4, 5])

print(np.isnan(arr))  # Output: [False False  True False False]
```

## Method 2: np.sum()

Another way to check for NaN is to use the np.sum() function, which adds up all the values in the array. NaN values are not counted in the sum and return NaN, so checking whether the sum is NaN is equivalent to checking whether there are NaN values in the array. This method is faster than np.isnan() for very large arrays, but it may be less readable. 

Example:

```
import numpy as np

arr = np.array([1, 2, np.nan, 4, 5])

print(np.sum(arr))  # Output: nan
print(np.isnan(np.sum(arr)))  # Output: True
```

## Method 3: np.any()

The np.any() function returns True if any value in the array is True. To use this function to check for NaN, we can apply np.isnan() to the array and then use np.any() to check if any True values are returned. This method is less efficient than np.isnan() and np.sum() because it applies two functions instead of one, but it may be more intuitive for some users. 

Example:

```
import numpy as np

arr = np.array([1, 2, np.nan, 4, 5])

print(np.any(np.isnan(arr)))  # Output: True
```

## Method 4: Looping

Although looping through an array is generally slow and discouraged in NumPy, it may be the best option for very small arrays, where overhead from a function call matters. This method can detect NaN faster than Boolean operation because it avoids the Boolean array creation overhead.

Example:

```
import numpy as np

arr = [1, 2, np.nan, 4, 5]

for item in arr:
    if np.isnan(item):
        print("NaN detected")
        break 
```

Alternatively, we can use python built-in math.isnan method in for loop. But, it might be slower than the Numpy methods when applied to large arrays.

Example:

```
import math
import numpy as np

arr = np.array([1, 2, np.nan, 4, 5])

for item in arr:
    if math.isnan(item):
        print("NaN detected")
        break 
```

Overall, np.isnan() is the preferred method for most cases. However, depending on the specific use case and the size of the array, the other methods may be faster and more efficient.
