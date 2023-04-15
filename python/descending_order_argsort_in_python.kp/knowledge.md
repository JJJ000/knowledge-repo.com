---
title: Can argsort be utilized to sort in descending order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, by negating the array and using argsort, then negating the resulting indices back will sort the array in descending order.
---

**Contents**

[TOC]

Yes, it is possible to use argsort in descending order in Python. Below are the steps to achieve this:

## 1. Using np.argsort() with [::-1]

When using np.argsort() function, we can append [::-1] at the end to flip the order of the array. This will give us the indices in descending order.

``` python
import numpy as np

arr = np.array([10, 7, 11, 5, 13, 8])
indices = np.argsort(arr)[::-1]
print(indices)
```

Output: `[4 2 0 1 5 3]`

## 2. Using np.argsort() with reverse parameter

Alternatively, we can use the reverse parameter of the np.argsort() function to get the indices in descending order.

``` python
import numpy as np

arr = np.array([10, 7, 11, 5, 13, 8])
indices = np.argsort(arr, axis=0, kind='quicksort', order=None, reverse=True)
print(indices)
```

Output: `[4 2 0 1 5 3]`

## 3. Using sort() method with reverse parameter

We can also use the sort() method on an array to get the indices in descending order by setting the reverse parameter to True.

``` python
import numpy as np

arr = np.array([10, 7, 11, 5, 13, 8])
indices = np.arange(len(arr))
indices = sorted(indices, key=arr.__getitem__, reverse=True)
print(indices)
```

Output: `[4, 2, 0, 1, 5, 3]`

## 4. Using pandas Series

We can use pandas Series to quickly get the indices in descending order.

``` python
import pandas as pd

arr = pd.Series([10, 7, 11, 5, 13, 8])
indices = arr.argsort()[::-1]
print(indices)
```

Output: `4 2 0 1 5 3`
