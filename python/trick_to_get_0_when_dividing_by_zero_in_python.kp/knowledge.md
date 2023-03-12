---
title: How can you achieve a result of 0 when dividing by zero?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You cannot return 0 with divide by zero in Python, as it would result in a ZeroDivisionError.
---

**Contents**

[TOC]

Section 1: Understanding the problem

Dividing any number by zero is undefined in Mathematics, hence it raises an error in Python. However, sometimes we might want to handle this error differently, and instead of terminating the program, we might want to return a specific value, such as zero. The question is how to return 0 with divide by zero in Python?

Section 2: Using try and except block

To handle the divide by zero error and return zero instead, we can enclose the division code inside a try and except block, and handle the ZeroDivisionError inside the except block. Here's an example:

```python
def divide(a, b):
    try:
        result = a/b
    except ZeroDivisionError:
        result = 0
    return result

# Test the function
print(divide(10, 5))    # Output: 2.0
print(divide(10, 0))    # Output: 0
```

In the above code, we define a function `divide` that takes two arguments `a` and `b`, and tries to divide `a` by `b`. If the division fails due to a ZeroDivisionError, we catch the error inside the except block and assign result to 0. If the division is successful, we return the result.

Section 3: Using a lambda function

We can also use a lambda function to handle the divide by zero error and return zero instead. Here's an example:

```python
divide = lambda a,b: 0 if b==0 else a/b

# Test the function
print(divide(10, 5))   # Output: 2.0
print(divide(10, 0))   # Output: 0
```

In the above code, we define a lambda function `divide` that takes two arguments `a` and `b`. If `b` is zero, we return 0, otherwise we divide `a` by `b` and return the result.

Section 4: Using NumPy

If you are working with arrays and matrices, you can use NumPy to handle the divide by zero error and return zero instead. Here's an example:

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([0, 2, 0])

result = np.divide(a, b, out=np.zeros_like(a), where=b!=0)

print(result)   # Output: [0. 1. 0.]
```

In the above code, we define two NumPy arrays `a` and `b` and use the `np.divide` function to divide `a` by `b`. We pass the optional arguments `out` as `np.zeros_like(a)` to initialise the result array with zeros, and `where` as `b!=0` to handle the divide by zero error and return zero instead.

Note: NumPy automatically suppresses the divide by zero warning when using `where` argument in `np.divide` function. This can sometimes hide errors in your code, so use it carefully.
