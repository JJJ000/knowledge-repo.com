---
title: What is the method to prevent the display of scientific notation while printing floating-point values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the format() function with the {} placeholder and the f specifier to print float values without scientific notation in Python.
---

**Contents**

[TOC]

1. Introduction
When working with floating point numbers in Python, we may encounter instances where the number is printed in scientific notation, which is not always desired. In this tutorial, we will discuss how to suppress scientific notation when printing float values in Python.

2. Using string formatting
One easy way to suppress scientific notation is to use string formatting. We can use the `format()` method to specify the precision with which the float value should be printed. Consider the following example:

```python
x = 123456789.123456789
print("{:.2f}".format(x))
```

In the above code, `"{:.2f}"` specifies that the float value should be printed with two digits after the decimal point. The output will be:

```
123456789.12
```

This method is useful when we want to print float values with a fixed number of decimal places.

3. Using the decimal module
Another way to suppress scientific notation is by using the `decimal` module in Python. This module provides greater precision when working with decimal values, and it can also be used to suppress scientific notation while printing. Consider the following example:

```python
from decimal import Decimal
x = Decimal("123456789.123456789")
print(x)
```

In the above code, we create a Decimal object by passing a string value to the `Decimal()` constructor. We then print the value of `x`, which will be:

```
123456789.123456789
```

This method is useful when we need to work with high-precision calculations involving decimal values.

4. Using NumPy
If we are working with arrays of float values, we can use NumPy to suppress scientific notation while printing. NumPy provides a `set_printoptions` function that allows us to customize the way float values are displayed. Consider the following example:

```python
import numpy as np
x = np.array([123456789.123456789, 0.00000000123456789])
np.set_printoptions(precision=18, suppress=True)
print(x)
```

In the above code, we create a NumPy array of two float values. We then use the `set_printoptions` function to specify that the precision should be 18 (i.e., all decimal places should be shown), and that scientific notation should be suppressed. The output will be:

```
[123456789.123456789   0.00000000123456789]
```

This method is useful when we are working with arrays of float values and want to customize the way they are displayed.
