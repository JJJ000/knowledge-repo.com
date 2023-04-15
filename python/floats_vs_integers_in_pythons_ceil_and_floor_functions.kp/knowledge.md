---
title: What is the reason behind python's math.ceil() and math.floor() operations returning floating-point values instead of integers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Python`s math.ceil() and math.floor() operations return floats instead of integers because they may involve fractional values when rounding up or down.
---

**Contents**

[TOC]

Introduction
Python provides two important functions to round off a number to the nearest integer, which are math.ceil() and math.floor(). These methods are used to round off the given floating-point number to the next integer (higher or lower) respectively. However, the question arises why these methods return floats instead of integers?

Explanation
Section 1: What is Math.ceil() and Math.floor()?

The math.ceil() function returns the smallest integer greater than or equal to the given number. It returns a float value representing the smallest possible integer value. The math.floor() function, on the other hand, rounds off the given number to the smallest integer value that is less than or equal to the given number.

Section 2: Why do they return a float value?

The reason for returning a float value is rooted in the fact that the arguments passed to these functions may be of different data types such as integers, floating points or other numeric types. Therefore, to accept all types of data as an argument, these functions return a floating point value.

Additionally, math.ceil() and math.floor() functions can accept fractional values (floats) as input. In such cases, the output of these functions will also be fractional (floats). Therefore, it is beneficial for these functions to return a floating-point value as output.

Section 3: Benefits of returning float values

Returning a float value has a significant advantage during mathematical operations as they are more precise than integers. As precision is critical in many mathematical applications, it is helpful when these functions return a float value.

Moreover, the use of floats instead of integers allows these functions to work with higher precision operations such as logarithms, exponents, and trigonometric functions, which can yield fractional values.

Section 4: Conclusion

In conclusion, the use of float values instead of integers in the math.ceil() and math.floor() functions is beneficial because it allows these functions to work with different data types and provides them with high precision. Therefore, Python's math library has implemented these functions to return floating-point values in their output.
