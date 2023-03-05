---
title: Steps to incorporate the softmax function into a Python code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Import the NumPy library and apply the softmax function to an array using np.exp().
---

**Contents**

[TOC]

# Overview

The softmax function is commonly used for multi-class classification. It takes an input vector of numerical scores and outputs a vector of probabilities that sum up to 1. In this tutorial, we will learn how to implement the softmax function in Python.

# Formula

The softmax function can be defined mathematically as:

$$softmax(x_i) = \frac{e^{x_i}}{\sum_{j=1}^{n} e^{x_j}}$$

where $x_i$ is the $i^{th}$ element of the input vector and $n$ is the length of the vector.

# Implementation

We can implement the softmax function as follows:

```python
import numpy as np

def softmax(x):
    """
    Compute the softmax of vector x

    Arguments:
        x: numpy array of shape (n,)

    Return:
        numpy array of shape (n,) containing softmax of each element of x
    """
    exp_x = np.exp(x)
    softmax_x = exp_x / np.sum(exp_x)

    return softmax_x
```

# Example

Let's test our implementation on a sample input array:

```python
x = np.array([1, 2, 3, 4, 1, 2, 3])
print("Softmax of x = ", softmax(x))
```

Output:

```
Softmax of x =  [0.02364054 0.06426166 0.1746813  0.47483299 0.02364054 0.06426166 0.1746813 ]
```

# Conclusion

In this tutorial, we learned how to implement the softmax function in Python for multi-class classification problems. The softmax function takes an input vector and returns a vector of probabilities. The numpy library is used for efficient array calculations.
