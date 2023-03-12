---
title: What is the method to iterate through the columns in a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use numpy`s transpose method to convert the rows of the array into columns and then use a for loop to iterate over them.
---

**Contents**

[TOC]

## Introduction
NumPy is a popular Python library used for numerical and scientific computations. It provides various functionalities to work with multi-dimensional arrays and matrices in Python. In this tutorial, we will see how to iterate over the columns of an array in NumPy.

## Creating an Array
Before we proceed to iterating over the columns of an array, let's first create an array. We can create a NumPy array using the `numpy.array()` function.

```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(arr)
```

Output:
```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

## Iterating over Columns
We can access the columns of the array using the index of the column. We can then loop over the columns using a for loop. Here is an example:

```python
for i in range(arr.shape[1]):
    col = arr[:, i]
    print(col)
```

Output:
```
[1 4 7]
[2 5 8]
[3 6 9]
```

In the above example, we use the `arr.shape[1]` to get the number of columns in the array. We then loop over the range of columns and extract each column using the `:` operator. The `:` operator selects all rows of a particular column. We then print the column using the `print()` function.

Another way to iterate over the columns of a NumPy array is by using the `numpy.nditer()` function. The `nditer()` function allows us to iterate over an array in a multi-dimensional fashion. Here is an example,

```python
for col in np.nditer(arr.T):
    print(col)
```

Output:
```
1
4
7
2
5
8
3
6
9
```

In the above example, we use the `nditer()` function on the transpose of the array. The `T` attribute of the array gets the transpose of the array. The `nditer()` function iterates over the array one element at a time. We then print the element using the `print()` function.

## Conclusion
In this tutorial, we saw how to iterate over the columns of a NumPy array in Python. We used a for loop to loop over the columns and the `nditer()` function to iterate over the columns.
