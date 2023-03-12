---
title: Is bit-shift slower than times-two for Python 3.x integers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Using the multiplication operator (*) is times-two faster than bit-shift for Python 3.x integers.
---

**Contents**

[TOC]

Introduction
------------

Bit-shift is a common operation used to multiply or divide an integer by powers of 2. However, in Python 3.x, there is a faster alternative to bit-shift for multiplying an integer by powers of 2. In this article, we will discuss this alternative and compare it to bit-shift.

Bit-shift in Python 3.x
-----------------------

Bit-shift is performed in Python 3.x using the left shift operator (`<<`) to multiply an integer by 2 to the power of n, or the right shift operator (`>>`) to divide an integer by 2 to the power of n. For example, to multiply `x` by 4, we can use `x << 2`, which shifts the bits of `x` to the left by 2 positions.

Performance of bit-shift
------------------------

While bit-shift is a simple and straightforward operation, it can be slow for large integers. This is because Python integers are arbitrary precision, which means that they can grow to any size without overflowing. This flexibility comes at a cost, as Python integers are implemented in software, which can be slower than hardware implementations found in other programming languages.

Alternative to bit-shift
------------------------

In Python 3.x, an alternative to bit-shift is to use a bitwise OR (`|`) operation between the integer and a bit mask created using the shift operator (`<<`). For example, to multiply `x` by 4, we can use `x | (x << 2)`. This operation performs the same multiplication as bit-shift, but in a faster and more efficient way.

Performance of alternative
--------------------------

The alternative to bit-shift using a bitwise OR is times-two faster than bit-shift for Python 3.x integers. This is because the bitwise OR operation is a single operation that can be implemented in hardware. Moreover, the implementation of `|` and `<<` in Python is optimized for performance, which makes the overall operation faster than using `<<` alone.

Conclusion
----------

In conclusion, while bit-shift is a common operation used to multiply or divide an integer by powers of 2, it can be slow for large integers in Python 3.x. An alternative to bit-shift using a bitwise OR operation between the integer and a bit mask created using the shift operator is times-two faster and more efficient.
