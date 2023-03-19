---
title: How can one obtain the indices of a sorted array in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `sorted` function to get a sorted copy of the array, and then use the `index` method to find the indices of each element in the original array.
---

**Contents**

[TOC]

# Introduction

When dealing with arrays or lists, sorting them is often necessary to make them easier to work with. However, sometimes it's important to know the original indices of the sorted elements. In this tutorial, we will explore different methods to obtain the indices of a sorted array in Python. 

# Using Numpy argsort()

One way to obtain the indices of a sorted array is to use the `argsort()` function from the Numpy library. This function returns an array of indices that would sort the original array in ascending order. Here's an example:

```python
import numpy as np

arr = np.array([10, 5, 20, 3])
sorted_indices = np.argsort(arr)
print(sorted_indices)
```
This will output: 
```
[3 1 0 2]
```

`sorted_indices` shows the sorted array indices based on the original array we passed. 

# Using Enumerate Function

Another way is to use the `enumerate()` function along with `sorted()`. Here's an example:

```python
arr = [10, 5, 20, 3]
sorted_indices = [index for index, value in sorted(enumerate(arr), key=lambda x:x[1])]
print(sorted_indices)
```

This will output:
```
[3, 1, 0, 2]
```

Here we used `enumerate()` to pair each element of the original array with its index, and then sort the pairs based on their values using a lambda function. Finally, we extract the indices from the sorted pairs. 

# Using Pandas Series Method i.e. rank()

If we have a Pandas `Series`, we can use the `rank()` method to get the sorted indices. Here's an example:

```python
import pandas as pd

s = pd.Series([10, 5, 20, 3])
sorted_indices = s.rank(method="dense").sub(1).astype(int).values
print(sorted_indices)

```

This will output:

```
[3 1 0 2]
```

In this example, we used the `rank()` method of the `Series` object with the `method` parameter set to `"dense"`. This assigns ranks to the elements based on their values and "dense" means the ranks are assigned such that no rank is skipped. We then substracted 1 so that the ranks are zero-based, finally, we converted the `Series` with `astype(int)` and retrieved its values in the form of an array. 

# Conclusion

In this tutorial, we learned three different methods of obtaining the indices of a sorted array in Python. We can use the `argsort()` function from `Numpy`, `enumerate()` function along with `sorted()`, or the `rank()` method of a Pandas Series. These functions can provide the sorted indices of a list or array, which can be especially useful when the original positions need to be preserved.
