---
title: When indexing what appears to be a number in python, what is the significance of "three dots"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: It signifies that the index is an extended slice that includes a range of values.
---

**Contents**

[TOC]

## Introduction
In Python, we can use indexing to access specific elements from a string or a list. Indexing is done by specifying the position of the element we want to access within the square brackets. However, sometimes we also see the use of "three dots" when indexing certain elements.

## The "three dots"
In Python, "three dots" or ellipsis (…) is used to represent a slice of all the remaining indices in a multi-dimensional array. It is more commonly used in NumPy arrays, but it can also be used in standard Python lists.

For example, consider the following NumPy array:

```python
import numpy as np

arr = np.array([[[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]]])
```

To access only the first element of each subarray, we can use the ellipsis to represent all the remaining dimensions:

```python
first_elem = arr[..., 0]
```

Here, the ellipsis represents all the remaining dimensions, and we are accessing only the first element from each subarray.

## Using "three dots" with indexing of integers
In Python, "three dots" can also be used while indexing an integer value. When we use "three dots" in this way, it represents the start or the end of a range.

For example, consider the following list:

```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
To get the first three elements of the list, we can use the following index:

```python
my_list[:3]
```
However, we can also use "three dots" to achieve the same result:

```python
my_list[:...3]
```
Here, the expression `...3` represents the range from the start of the list to the third element.

## Conclusion
"Three dots" in Python is a versatile tool that can be used in many different contexts, especially while indexing multi-dimensional arrays. It is important to keep in mind that the use of "three dots" may not be appropriate in all situations and can sometimes lead to unintended results.
