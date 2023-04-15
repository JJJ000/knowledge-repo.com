---
title: What is the functionality of the modulo (%) operator on negative numbers in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The modulo operator (%) works the same way on negative numbers as it does on positive numbers, returning the remainder after division.
---

**Contents**

[TOC]

### Basic functionality of modulo operator

The modulo operator (%) in Python returns the remainder of the division of two integers. For example, 10 % 3 returns 1 because when 10 is divided by 3, there is a remainder of 1. 

### Modulo operator on positive numbers

When the modulo operator is used on positive numbers, it works as expected. For example, 5 % 3 returns 2 because 5 divided by 3 leaves a remainder of 2.

### Modulo operator on negative numbers

When the modulo operator is used on negative numbers, the result can be a bit unexpected. The result is still the remainder of the division, but it may not be what one would expect.

For example, -5 % 3 returns 1, not -2 as one might expect. This is because the modulo operator in Python always returns a value that has the same sign as the divisor. In this case, the divisor is 3, which is positive, so the result is also positive.

Similarly, 5 % -3 returns -1, not 2 as one might expect. This is because the divisor is -3, which is negative, so the result is also negative.

### Caveats when using modulo operator on negative numbers

When the modulo operator is used on negative numbers, it is important to understand how it works so that unexpected results can be avoided.

One caveat to keep in mind is that the sign of the divisor matters. As mentioned earlier, the result of the modulo operation will have the same sign as the divisor.

Another caveat is that the result of the modulo operation will always be less than the absolute value of the divisor. For example, -5 % 3 returns 1 because the absolute value of 3 is 3, and 1 is less than 3.

To avoid unexpected results when using the modulo operator on negative numbers, it is important to keep these caveats in mind and adjust the operands accordingly.
