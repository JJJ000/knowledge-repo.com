---
title: What is the method to obtain the digits succeeding the decimal point?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To get numbers after the decimal point in Python, use the modulus operator (%).
---

**Contents**

[TOC]

## Getting Numbers After Decimal Point in Python

Getting the numbers after the decimal point in Python can be done in various ways. Here are some of them:

### Method 1: Using the modulo operator

One way to get the numbers after the decimal point in Python is by using the modulo operator. The modulo operator (%) returns the remainder of a division operation. 

```python
number = 13.57
decimal_part = number % 1
print(decimal_part) # Output: 0.57
```

### Method 2: Using the math module

Another way to get the numbers after the decimal point in Python is using the math module. The math module provides a function floor() that returns the largest integer less than or equal to a given number. By subtracting the original number from the floor of the number, we get the decimal part.

```python
import math

number = 13.57
decimal_part = number - math.floor(number)
print(decimal_part) # Output: 0.57
```

### Method 3: Using string manipulation

A third way to get the numbers after the decimal point in Python is by converting the number into a string and then manipulating it. We can use the string method split() to split the string at the decimal point and then retrieve the second element of the resulting list.

```python
number = 13.57
decimal_part = str(number).split('.')[1]
print(decimal_part) # Output: 57
```

### Method 4: Using the fractional module

Python also has a built-in module called fractional that can be used to represent and manipulate fractions. We can use the Fraction constructor to create a fraction object and then retrieve its numerator and denominator using the numerator and denominator attributes.

```python
from fractions import Fraction

number = 13.57
fraction = Fraction(number).limit_denominator()
decimal_part = fraction.numerator % fraction.denominator
print(decimal_part) # Output: 57
```

Note: The limit_denominator() method is called to approximate the decimal number as a fraction with a denominator that does not exceed a certain value (by default 1000000). This is necessary because the exact representation of a decimal number as a fraction is not always possible.
