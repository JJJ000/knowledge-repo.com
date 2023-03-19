---
title: How to obtain a random subset of rows from a 2d array using numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use numpy.random.choice() to randomly select a subset of rows from a 2D numpy array.
---

**Contents**

[TOC]

## Section 1: Introduction

NumPy provides a lot of functionality to work with arrays in Python. One common task is to generate a random set of rows from a 2D array. This can be useful, for example, when you want to sample some data from a larger dataset to perform analysis or modeling. In this tutorial, we will explore how to use NumPy to randomly sample rows from a 2D array, and discuss different approaches to achieve this.

## Section 2: Using numpy.random.choice

The simplest approach is to use the `numpy.random.choice()` function to select random indices from the first dimension of the array. The function takes an array and the number of indices to select, and returns an array of indices that can be used to select the corresponding rows. Here's an example:

```python
import numpy as np

# create a 2D array
a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# select 2 random rows
rows = np.random.choice(a.shape[0], size=2, replace=False)

# select the rows from the array
result = a[rows, :]

print(result)
```

Output:
```
array([[7, 8, 9],
       [1, 2, 3]])
```

In this example, we first create a 2D array `a`. Then, we use `np.random.choice()` to select 2 random indices from the first dimension (`a.shape[0]` gives the size of the first dimension of `a`). In this case, we set `replace=False` to select each row only once. Finally, we select the rows corresponding to these indices from `a` using slicing (`a[rows, :]`), which gives us the desired result.

## Section 3: Using numpy.random.shuffle

Another approach is to use the `numpy.random.shuffle()` function to randomly shuffle the array along the first dimension, and then select the first `k` rows. Here's an example:

```python
import numpy as np

# create a 2D array
a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# shuffle the array along the first dimension
np.random.shuffle(a)

# select the first 2 rows
result = a[:2, :]

print(result)
```

Output:
```
array([[7, 8, 9],
       [4, 5, 6]])
```

In this example, we first create a 2D array `a`. Then, we use `np.random.shuffle()` to randomly shuffle the rows of `a`. Finally, we select the first 2 rows using slicing (`a[:2, :]`), which gives us the desired result. Note that this approach may modify the original array, which may not be desirable in some cases.

## Section 4: Conclusion

In this tutorial, we have explored two approaches to randomly sample rows from a 2D array using NumPy. The first approach uses `numpy.random.choice()` to select random indices from the first dimension, and then select the corresponding rows using slicing. The second approach uses `numpy.random.shuffle()` to randomly shuffle the array along the first dimension, and then select the first `k` rows using slicing. Both approaches have their advantages and can be useful depending on the context.
