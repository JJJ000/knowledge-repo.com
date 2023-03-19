---
title: Is there a Python counterpart of // operator for ceiling values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: No, there is no ceiling equivalent of the // operator in Python.
---

**Contents**

[TOC]

Ceiling Equivalent of // Operator in Python

Python provides a floor division operator (//) that returns the quotient of the division of two numbers, rounded down to the nearest integer. However, there is no built-in ceiling division operator in Python. A ceiling division operation would perform the division of two numbers and round up the result to the nearest integer.

Section 1: Ceil Function

Python provides the math.ceil() function, which returns the smallest integer greater than or equal to a given number. We can use this function to perform the ceiling division operation as follows:

```python
import math

result = math.ceil(dividend / divisor)
```

Here, dividend and divisor are the two numbers we want to divide, and result is the rounded-up quotient of the division.

Section 2: Custom Function

If we do not want to import the math module, or we want to define our own custom function, we can use the following code:

```python
def ceil_division(dividend, divisor):
    quotient = dividend / divisor
    if quotient > 0:
        return int(quotient) + 1
    else:
        return int(quotient)
```

This function first performs the regular division of the two numbers and checks if the quotient is greater than zero. If it is, it rounds up the quotient by adding one to the integer part. If the quotient is zero or negative, it returns the integer part.

Section 3: NumPy Function

The NumPy library provides a ceiling division function called np.ceil_divide(). This function takes two arrays as input and returns the element-wise ceiling division of the two arrays.

```python
import numpy as np

result = np.ceil_divide(dividend_array, divisor_array)
```

Here, dividend_array and divisor_array are two NumPy arrays of the same shape, and result is the array of rounded-up quotients.

Section 4: Third-Party Libraries

There are several third-party libraries available that provide additional mathematical functions, including ceiling division. These libraries include SymPy, mpmath, and Fraction. However, for most purposes, the math.ceil() function or the custom function described in Section 2 should be sufficient.
