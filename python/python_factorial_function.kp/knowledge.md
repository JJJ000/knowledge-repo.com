---
title: Python code to calculate factorial
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The function for factorial in Python is math.factorial().
---

**Contents**

[TOC]

# Definition

Factorial of a non-negative integer `n`, is the product of all positive integers less than or equal to `n`. It is denoted by `n!`. For example, `5!` means `5 * 4 * 3 * 2 * 1` which is `120`.

# Naive approach

The factorial of a number can be calculated using a simple loop that multiplies the current value with a variable that stores the product until the loop terminates. Here's the code for the naive approach:

```
def factorial_naive(n):
    result = 1
    for i in range(1, n+1):
        result = result * i
    return result
```

However, this approach can be slow for large input values as it involves a loop that iterates `n` times.

# Recursive approach

Another way to implement the factorial function is through recursion. In this approach, the function calls itself with smaller input values until it reaches a base case. Here's the code for the recursive approach:

```
def factorial_recursive(n):
    if n == 0:
        return 1
    else:
        return n * factorial_recursive(n-1)
```

This approach is elegant and easy to understand. However, it can have performance issues for large input values due to the way recursion works.

# Math module approach

Python's `math` module provides a built-in `factorial` function that can be used to calculate the factorial of a number. Here's the code to use the `factorial` function:

```
import math

def factorial_math(n):
    return math.factorial(n)
```

This approach is the most efficient as it utilizes a built-in function that is optimized for performance. However, it has a limitation of being unable to handle values larger than the maximum integer supported by the system.
