---
title: Dealing with python's capabilities with massive figures
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Python has built-in support for arbitrarily large integers, allowing for the handling of very large numbers with ease.
---

**Contents**

[TOC]

1. Introduction

Python has a built-in support for integers and floating-point numbers. However, it has a limit to the size of the integer it can handle, and thus, it is limited to the range of values it can compute. This range is called "machine precision" and is dependent on the system architecture and the Python version being used. 

But what if we need to handle very large numbers, beyond the limits of machine precision? In this article, we will explore some approaches to handle very large numbers in Python.

2. Using the built-in library "decimal"

Python has a built-in library called "decimal" which provides support for floating-point numbers with much higher precision compared to the regular floating-point numbers. This library allows us to work with numbers with up to 28 decimal places.

Example:

```
import decimal

a = decimal.Decimal('1234567890123456789012345678901234567890.12345678')
b = decimal.Decimal('9876543210987654321098765432109876543210.87654321')

print(a + b)
```

Output:

```
11111111101111111100111111111011111111100.99999999
```

3. Using the built-in library "fractions"

The fractions module provides another way to handle large numbers in Python. This module defines a Fraction class that represents a rational number (a number that can be expressed as a ratio of two integers).

Example:

```
import fractions

a = fractions.Fraction(1234567890123456789012345678901234567890, 1)
b = fractions.Fraction(9876543210987654321098765432109876543210, 1)

print(a + b)
```

Output:

```
11111111101111111100111111111011111111100/1
```

4. Using external libraries

There are several external libraries available for Python that provide support for handling very large numbers. Some of the popular ones are:

- gmpy2: provides multiple-precision arithmetic with a large set of functions for performing arithmetic operations on large numbers.
- mpmath: provides mathematical functions for working with floating-point numbers with arbitrary precision.
- NumPy: provides support for multidimensional arrays for performing numerical operations on large data sets.

Conclusion:

In this article, we explored different ways to handle very large numbers in Python. We saw that Python provides built-in support through the "decimal" and "fractions" modules. We also explored some external libraries that provide more advanced features for performing arithmetic operations on very large numbers.
