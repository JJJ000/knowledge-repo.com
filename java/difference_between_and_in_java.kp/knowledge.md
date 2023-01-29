---
title: The difference between '>>>' and '>>' is that '>>>' is a prompt used in the Python interpreter, while '>>' is a prompt used in the JavaScript interpreter
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `>>` operator is a bitwise right shift operator, while the `>>>` operator is a bitwise unsigned right shift operator.
---

**Contents**

[TOC]

### Difference in Bitwise Operators

The >>> operator is known as the unsigned right shift operator in Java, while the >> operator is known as the signed right shift operator. 

The difference between the two is that the >>> operator shifts the bits of a number to the right by a specified number of times and appends 0s at the left side, whereas the >> operator shifts the bits of a number to the right by a specified number of times and appends the sign bit at the left side.

### Difference in Results

The result of the >>> operator is always a positive number, while the result of the >> operator can be either a positive or a negative number depending on the sign bit of the number. 

For example, if the number is 4 (in binary 100) and the shift is 1, the result of the >> operator will be 2 (in binary 10) and the result of the >>> operator will be 2 (in binary 10) as well. However, if the number is -4 (in binary 1111 1111 1111 1111 1111 1111 1111 1100) and the shift is 1, the result of the >> operator will be -2 (in binary 1111 1111 1111 1111 1111 1111 1111 1110) and the result of the >>> operator will be 2147483646 (in binary 0111 1111 1111 1111 1111 1111 1111 1110).

### Difference in Usage

The >> operator is mainly used for arithmetic operations, while the >>> operator is mainly used for logical operations. 

For example, the >> operator can be used to divide a number by two, while the >>> operator can be used to count the number of trailing zeroes in a number.
