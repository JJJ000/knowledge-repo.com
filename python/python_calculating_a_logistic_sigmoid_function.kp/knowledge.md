---
title: What is the process of computing a logistic sigmoid function using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The logistic sigmoid function can be calculated in Python using the NumPy library, by applying the expit() function on the input values.
---

**Contents**

[TOC]

## Section 1: Understanding the Logistic Sigmoid Function

The logistic sigmoid function is a mathematical function that maps any input value between 0 and 1. This function is widely used in machine learning and deep learning to model the probability of a binary outcome.

The logistic sigmoid function is defined as:

$$\sigma(x) = \frac{1}{1 + e^{-x}}$$

where x is the input value and $\sigma(x)$ is the output value between 0 and 1.

## Section 2: Writing the Python Function

To calculate the logistic sigmoid function in Python, we can define a function as follows:

```
import math

def sigmoid(x):
    return 1 / (1 + math.exp(-x))
```

In this function, we use the math library to calculate the exponential function, which is denoted by `math.exp()`. We then return the value of the logistic sigmoid function using the above formula.

## Section 3: Example Usage

We can now use the sigmoid function to calculate the logistic sigmoid value of any input value. For example:

```
print(sigmoid(0))    # Output: 0.5
print(sigmoid(1))    # Output: 0.7310585786300049
print(sigmoid(-1))   # Output: 0.2689414213699951
```

In the above example, we have calculated the sigmoid function for input values of 0, 1, and -1.

## Section 4: Conclusion

In this tutorial, we have learned how to calculate the logistic sigmoid function in Python. This function is useful in modeling the probability of a binary outcome in machine learning and deep learning.
