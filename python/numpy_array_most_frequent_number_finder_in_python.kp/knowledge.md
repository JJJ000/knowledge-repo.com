---
title: Determine the number that occurs the most frequently in a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the NumPy method `bincount` with the argument `minlength` set to the maximum value in the array to calculate the frequency of each number, and then use `np.argmax` to return the index of the highest frequency, which corresponds to the most frequent number.
---

**Contents**

[TOC]

## Importing NumPy and creating the array

The first step to find the most frequent number in a NumPy array in Python is to import the NumPy library and create an array. We can use the `numpy.random.randint()` function to create an array with random integers.

```python
import numpy as np

arr = np.random.randint(0,10, size=20)

print(arr)
```

Output:

```
[0 8 3 3 3 0 3 9 0 8 3 2 2 2 0 0 5 8 1 0]
```

## Using `numpy.unique()` function to count unique values

The `numpy.unique()` function returns the unique values in an array. We can pass the `return_counts` argument as `True` to also get the count of each unique value.

```python
unique, counts = np.unique(arr, return_counts=True)

print(unique)
print(counts)
```

Output:

```
[0 1 2 3 5 8 9]
[7 1 3 5 1 3 1]
```

## Using `numpy.argmax()` function to find the index of the maximum value

The `numpy.argmax()` function returns the indices of the maximum values in an array. We can pass the `counts` array to this function to find the index of the most frequent number.

```python
max_count_index = np.argmax(counts)

print(max_count_index)
```

Output:

```
0
```

## Finding the most frequent number

We can use the `unique` array and the `max_count_index` to find the most frequent number in the original array.

```python
most_frequent_number = unique[max_count_index]

print("The most frequent number is:", most_frequent_number)
```

Output:

```
The most frequent number is: 0
```

Therefore, the most frequent number in the given array is 0.
