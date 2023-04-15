---
title: Can you explain the distinction between contiguous and non-contiguous arrays?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Contiguous arrays have elements stored in adjacent memory locations, while non-contiguous arrays have scattered elements stored at different locations in memory.
---

**Contents**

[TOC]

Contiguous Arrays in Python

A contiguous array in Python is also called a C-style array. A contiguous array is a one-dimensional array where each element in the array is stored in adjacent memory locations. Thus, the location of a value in a contiguous array can be calculated using the following formula:

    location = base_address + (index * element_size)

A contiguous array is preferred for array operations as it allows for efficient memory management and CPU caching. This means that operations on a contiguous array are much faster than operations on a non-contiguous array. 

Non-contiguous Arrays in Python

A non-contiguous array in Python is also called a strided array. In a non-contiguous array, the elements are not stored in adjacent memory locations. Instead, the elements are stored in a sequence of evenly spaced steps or "strides". This means that the location of a value in a non-contiguous array cannot be calculated using a simple formula like for a contiguous array. 

Non-contiguous arrays are often used when dealing with multi-dimensional arrays, as they allow for more efficient packing of data. However, operations on non-contiguous arrays are generally slower than operations on contiguous arrays due to the additional overhead required to access the scattered elements.

Examples of contiguous and non-contiguous arrays

Here's an example of creating a contiguous array using Numpy:

```python
import numpy as np 

# Creating a contiguous array
arr1 = np.arange(10)
print(arr1)

# Output: [0 1 2 3 4 5 6 7 8 9]
```

In the example above, we use the `arange()` function from Numpy to create a contiguous array.

Now let's create a non-contiguous array:

```python
# Creating a non-contiguous array using strides
arr2 = np.zeros((5,5), dtype=float)[::2, ::2]
print(arr2)

# Output:
# [[0. 0.]
#  [0. 0.]]
```

In the example above, we use the `zeros()` function from Numpy to create a 5x5 matrix filled with zeros. We then select only every other row and column to create a non-contiguous array of shape (2,2). 

Conclusion

In summary, a contiguous array is a one-dimensional array where each element is stored in adjacent memory locations, while a non-contiguous array is a multi-dimensional array where elements are stored in a sequence of strides. Operations on a contiguous array are generally faster than operations on a non-contiguous array, but non-contiguous arrays are often used when dealing with multi-dimensional arrays.
