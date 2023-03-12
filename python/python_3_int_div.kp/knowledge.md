---
title: An alternative wording for 'python 3 integer division' could be 'division operation that produces integer output in Python 3'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Python 3 integer division using the double forwardslash (//) operator returns the quotient of a division, rounded down to the nearest integer.
---

**Contents**

[TOC]

# Introduction

Python 3 has two types of division: floating-point division and integer division. In this article, we’ll focus on Python 3 integer division.


# Definition

Integer division (also known as floor division) is a division operation where the quotient is rounded towards negative infinity (i.e., rounded down) to the nearest integer. In Python 3, integer division is denoted using the double forward slash operator (//).


# Example

```
a = 7
b = 2
c = a // b
print(c)
```

Output: 3

In the above code, we’re performing integer division between `a` and `b`. The quotient is `3`, which is the largest integer that is less than or equal to the result of dividing `a` by `b`.


# Summary

Python 3 integer division returns the quotient of a division operation rounded towards negative infinity. It is denoted using the double forward slash (//) operator.
