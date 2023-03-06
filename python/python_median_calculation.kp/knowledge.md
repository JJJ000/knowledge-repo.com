---
title: Rewording 'python code for determining the middle value of a list'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the median() function from the statistics module to find the median of a list in Python.
---

**Contents**

[TOC]

# Introduction

In statistics, the median of a list is the value that separates the higher and lower values of that list into equal halves. It's a measure of central tendency that is more robust to outliers than the mean. In Python, there are several ways to find the median of a list, depending on the tools and libraries you're using. This tutorial will cover some of the most common and widely used methods.

# Method 1: Sorting and Indexing

One of the simplest and most intuitive ways to find the median of a list in Python is to first sort the list in ascending or descending order, and then take the middle value or average of the two middle values, depending on whether the list has an odd or even length. Here's an example code snippet:

```
def median(lst):
    n = len(lst)
    s = sorted(lst)
    return (s[n//2] + s[-(n//2+1)]) / 2

lst = [4, 2, 5, 1, 3]
print(median(lst))  # output: 3
```

In this method, we first obtain the length of the list `n`, sort the list using the built-in `sorted()` function, and then return the median value computed as the average of the two middle values using integer division `//`. Note that we're using the negative index `-1` to access the last element of the sorted list, since Python indices start at 0.

# Method 2: Using Statistics Module

Another way to find the median of a list in Python is to use the `median()` function provided by the `statistics` module, which was introduced in Python 3.4. This function takes a list as input and returns the median value, using the same algorithm as Method 1 but with a more concise and optimized implementation. Here's an example code snippet:

```
import statistics as stats

lst = [4, 2, 5, 1, 3]
print(stats.median(lst))  # output: 3
```

In this method, we simply import the `statistics` module and call the `median()` function, passing the list as an argument. The function returns the median value directly, without the need for additional computation.

# Method 3: Using Numpy Module

Finally, a third way to find the median of a list in Python is to use the `median()` function provided by the `numpy` module, which is a powerful library for numerical computing and data analysis. This method is especially useful if you're working with large or multidimensional arrays, or if you need additional features and functionality beyond simple median computation. Here's an example code snippet:

```
import numpy as np

lst = [4, 2, 5, 1, 3]
print(np.median(lst))  # output: 3
```

In this method, we import the `numpy` module and alias it as `np`, then call the `median()` function, passing the list as an argument. The function returns the median value directly, using an optimized implementation that can handle various data types and array shapes. Note that this method requires `numpy` to be installed on your system, which you can do using pip or conda.
