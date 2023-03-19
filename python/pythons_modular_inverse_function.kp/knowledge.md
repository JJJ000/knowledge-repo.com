---
title: The Python implementation of a function that calculates the modular multiplicative inverse
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The modular multiplicative inverse function in Python can be implemented using the extended Euclidean algorithm.
---

**Contents**

[TOC]

I. Introduction
The modular multiplicative inverse of an integer "a" modulo "m" is an integer "x" such that the product (a*x) is congruent to 1 modulo "m". In other words, it is the number that can be multiplied by "a" to get a multiple of "m" plus 1.

II. Using the Extended Euclidean Algorithm
One way to find the modular multiplicative inverse of "a" modulo "m" is to use the extended Euclidean algorithm. This involves finding the greatest common divisor of "a" and "m", and then using the coefficients in the Bezout's identity to calculate the inverse.

```python
def extended_gcd(a, b):
    if a == 0:
        return (b, 0, 1)
    else:
        gcd, x, y = extended_gcd(b % a, a)
        return (gcd, y - (b // a) * x, x)

def mod_inverse(a, m):
    gcd, x, y = extended_gcd(a, m)
    if gcd != 1:
        raise ValueError("No modular inverse exists")
    else:
        return x % m
```

III. Using Fermat's Little Theorem
If "m" is a prime number, then the modular multiplicative inverse of "a" modulo "m" is given by a^(m-2) modulo "m". We can use this fact to compute the inverse as follows:

```python
def mod_inverse(a, m):
    if gcd(a, m) != 1:
        raise ValueError("No modular inverse exists")
    else:
        return pow(a, m-2, m)
```

IV. Conclusion
In this tutorial, we discussed two ways to compute the modular multiplicative inverse of an integer "a" modulo "m" in Python. The first method uses the extended Euclidean algorithm, while the second method uses Fermat's little theorem. The choice of method depends on the requirements of the specific application.
