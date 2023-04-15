---
title: Reducing the number of entries in a numpy array by selecting every nth entry
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To subsample every nth entry in a numpy array in Python, you can use array slicing with the step parameter.
---

**Contents**

[TOC]

Section 1: Introduction
One common task in data analysis is sub-sampling, where we select every nth item from a dataset. In Python, this task can be accomplished easily with the use of the NumPy library. In this tutorial, we will cover how to subsample every nth entry in a NumPy array.

Section 2: Creating a Sample NumPy Array
Before we can start subsampling, we need to create a sample NumPy array. Here is an example of a NumPy array with 20 integers:

```python
import numpy as np
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20])
```

Section 3: Subsampling Nth Entries in a NumPy Array
To subsample every nth entry in our NumPy array, we can use the following code:

```python
n = 3
subsampled_arr = arr[::n]
```

In this code, we set the value of n to 3, which means every third entry will be selected. The subsampled_arr variable will contain the following values:

```python
[1 4 7 10 13 16 19]
```

Section 4: Conclusion
In this tutorial, we learned how to subsample every nth entry in a NumPy array using Python. We used NumPy's slicing functionality to select every nth element from our array and created a new array with the subsampled elements. This is a common data analysis technique that can help us to efficiently analyze large datasets.
