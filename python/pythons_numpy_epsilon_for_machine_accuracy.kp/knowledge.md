---
title: Machine epsilon for Python using numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Numpy machine epsilon is the smallest number that can be added to 1.0 and still be represented as a different number in the floating point system used by the computer.
---

**Contents**

[TOC]

Introduction to Machine Epsilon

In computer science, machine epsilon is the smallest value that can be added to 1 in the floating-point representation of a computer. This value is important in understanding the limits of the numerical stability of algorithms and the uncertainty associated with the representation of real numbers in a computer's memory. Python has a mathematical library called NumPy that provides various functions to deal with floating-point numbers, including machine epsilon. In this article, we will explore how to compute machine epsilon in NumPy.

Computing Machine Epsilon

NumPy provides a function called "finfo" that returns various information about the floating-point format used by the computer. One of the values returned by finfo is "eps," which is the machine epsilon. Here is an example of how to use finfo to compute the machine epsilon:

``` python
import numpy as np

eps = np.finfo(float).eps

print(eps)
```

This code will output the machine epsilon value for the computer's floating-point format.

Interpreting Machine Epsilon

The machine epsilon value returned by NumPy's finfo function is the smallest value that can be added to 1 to produce a value that is different from 1. This means that any value smaller than the machine epsilon is effectively considered to be 0 by the computer. It is important to remember that the machine epsilon refers to the precision of the floating-point format used by the computer, and not the precision of the actual calculation being performed. In practice, the precision of a calculation may be limited due to other factors such as the quality of the algorithm being used, the range of values being calculated, and the rounding errors introduced by successive calculations.

Conclusion

In this article, we have seen how to compute the machine epsilon value for a floating-point format using NumPy's finfo function. The machine epsilon value is an important concept in understanding the limits of computational precision and the uncertainty associated with the representation of real numbers in a computer's memory. While the machine epsilon provides some guidance on the limits of numerical accuracy, it is important to keep in mind that the precision of a calculation may be limited by other factors as well.
