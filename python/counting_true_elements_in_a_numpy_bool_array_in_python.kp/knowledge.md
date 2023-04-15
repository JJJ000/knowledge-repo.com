---
title: What is the method to determine the quantity of true elements within a numpy boolean array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the count\_nonzero() method from NumPy to count the number of true elements in a bool array.
---

**Contents**

[TOC]

## 1. Creating a boolean array in NumPy

Before we can count the number of true elements in a bool array in NumPy, we need to create a bool array first. We can create a bool array in NumPy by using the `numpy.array()` function and specifying the `dtype` parameter as 'bool'. 

```
import numpy as np

# create a bool array
bool_array = np.array([True, False, True, True], dtype=bool)
print(bool_array)
```
Output:
```
[ True False  True  True]
```

## 2. Counting the number of true elements in the bool array

Now that we have a bool array, we can count the number of true elements in the array by using the `numpy.count_nonzero()` function. This function returns the number of non-zero elements in the input array.

```
import numpy as np

# create a bool array
bool_array = np.array([True, False, True, True], dtype=bool)

# count the number of true elements
count = np.count_nonzero(bool_array)

print("Number of true elements: ", count)
```

Output:
```
Number of true elements:  3
```

## 3. Example with a larger bool array

Let's try an example with a larger bool array.

```
import numpy as np

# create a bool array of length 10
bool_array = np.array([True, False, True, True, False, False, True, False, True, True], dtype=bool)

# count the number of true elements
count = np.count_nonzero(bool_array)

print("Number of true elements: ", count)
```

Output:
```
Number of true elements:  6
```

## 4. Summary

To count the number of true elements in a NumPy bool array in Python, we can use the `numpy.count_nonzero()` function. This function returns the number of non-zero elements in the input array. Before we can count the number of true elements, we need to create a bool array in NumPy by using the `numpy.array()` function and specifying the `dtype` parameter as 'bool'.
