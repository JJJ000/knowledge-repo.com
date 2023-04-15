---
title: In Python 3, why is the floating-point representation of 4*0.1 aesthetically pleasing, while that of 3*0.1 is not?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This is because 0.1 cannot be precisely represented in binary floating-point, resulting in rounding errors that accumulate differently for different calculations.
---

**Contents**

[TOC]

Background: Floating-Point Arithmetic

Floating-point arithmetic is used to represent and perform calculations with numbers that have a fractional component. In computing, floating-point numbers are typically represented using the IEEE 754 standard. However, due to the way that floating-point numbers are stored and processed, rounding and approximation errors can occur when performing calculations with them.

Section 1: The Representation of 0.1 in Binary

One key factor in the phenomenon observed is the way that the number 0.1 is represented in binary. In decimal (base 10) notation, 0.1 is an infinitely repeating fraction: 0.1 = 1/10 = 0.100000... In binary (base 2) notation, however, 0.1 is not an exact value - it is an infinitely repeating fraction in binary as well: 0.1 (base 10) = 0.00011001100110011... (base 2). 

Section 2: The Representation of Multiplication Results in Binary

When we multiply 0.1 by 3 or 4, we are essentially summing three or four copies of the infinite binary fraction 0.1, i.e., 0.1 + 0.1 + 0.1 = 0.3 or 0.1 + 0.1 + 0.1 + 0.1 = 0.4 . Due to the nature of the IEEE 754 floating-point representation, the result of this summation can sometimes be closer to the exact mathematical result than at other times.

Section 3: Floating-Point Rounding Errors

Although the binary sum of 0.1 may be very accurate when multiplying by 4 (which is a power of 2, and whose binary representation can be expressed exactly), the same may not hold true when multiplying by 3 - this is because the binary representation of 3 is not an exact power of 2. When 3 * 0.1 is calculated using IEEE 754 floating-point arithmetic, rounding errors can occur, leading to a result that is not exactly equal to the mathematically exact value.

Section 4: Summary

In summary, the reason why the floating-point value of 4*0.1 looks nice in Python 3 but 3*0.1 doesn't can be attributed to a combination of factors, including the way that 0.1 is represented in binary, the way that multiplication results are represented in binary, and the nature of floating-point rounding errors. While the binary sum of 0.1 may be very accurate when multiplying by 4 due to the representation of 4 as a power of two, this may not hold true when multiplying by 3, leading to rounding errors in the result.
