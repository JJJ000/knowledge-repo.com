---
title: Rewording formatting decimal numbers without any zeros at the end
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `g` format specifier in the format() method, or use the f-string method with the same specifier `{g}`.format(my\_float) or f`{my\_floatg}`.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides numerous formatting options for numbers. By default, floats in Python contain a fixed amount of digits after the decimal point. But there are times when we would like to remove trailing zeros from these numbers.

In this answer, we will explore different techniques to format floats without trailing zeros using Python.

Section 2: Using the format() method
Python's format() method provides a way to format numbers to a specified number of decimal places. We can use the  '{:.0f}' format specifier to specify that the float should be printed without any decimal places. This will automatically remove any trailing zeros at the end.

```python
num = 12.3400
formatted_num = '{:.0f}'.format(num)
print(formatted_num)
```
Output: 12

Section 3: Using the str.rstrip() method
Another way to remove trailing zeros from a float is to convert it to a string and then use the rstrip() method to remove the zeros. We can use the split() method to split the string into two parts - the integer part and the decimal part. Then, we can use the rstrip() method to remove any zeros from the decimal part.

```python
num = 12.3400
formatted_num = str(num).rstrip('0').rstrip('.')
print(formatted_num)
```
Output: 12.34

Section 4: Using the decimal module
The decimal module in Python provides additional precision compared to floats. We can use the decimal.Decimal class to convert a float to a decimal number and then use the normalize() method to remove trailing zeros. The normalize() method returns the number in its simplest form.

```python
from decimal import Decimal

num = 12.3400
formatted_num = Decimal(str(num)).normalize()
print(formatted_num)
```
Output: 12.34

Section 5: Conclusion
In this answer, we explored different techniques to format floats without trailing zeros using Python. By using the format() method, str.rstrip() method, and the decimal module, we can easily remove trailing zeros and format floats according to our needs.
