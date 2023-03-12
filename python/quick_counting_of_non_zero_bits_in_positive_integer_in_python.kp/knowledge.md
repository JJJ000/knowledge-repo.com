---
title: A quick method for calculating the number of non-zero bits in a positive integer
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the built-in `bin()` function to convert the integer to binary, then count the number of `1` characters using the string method `count()`.
---

**Contents**

[TOC]

1. Using Bitwise Operations:
We can use bitwise operations to count the number of non-zero bits in a positive integer. First, we convert the integer to its binary representation using the `bin()` function. Then, we count the number of `1`'s in the binary representation using the bitwise AND (`&`) operation and a mask that has all `1`'s in its binary representation except in the least significant bit, which is set to `0`. Here's an example implementation:

```python
def count_nonzero_bits(n):
    bin_n = bin(n)
    count = 0
    mask = 0b11111111111111111111111111111110 # all 1's except least significant bit
    while n > 0:
        count += n & 1
        n >>= 1
    return count
```

2. Using the bit-counting algorithm:
We can also use the bit-counting algorithm to count the number of non-zero bits in a positive integer. This algorithm works by repeatedly masking out the least significant `1` bit of the integer and incrementing the count until the integer becomes `0`. Here's an example implementation:

```python
def count_nonzero_bits(n):
    count = 0
    while n > 0:
        count += 1
        n &= n - 1  # mask out least significant 1 bit
    return count
```

3. Using built-in functions:
Python provides several built-in functions that can be used to count the number of non-zero bits in a positive integer. One of them is the `bin()` function, which returns the binary representation of an integer as a string. We can count the number of `1`'s in the binary representation using the `count()` method of the string. Here's an example implementation:

```python
def count_nonzero_bits(n):
    bin_n = bin(n)
    return bin_n.count('1')
```

4. Using the built-in `popcount()` function:
Starting from Python 3.10, the `int` class has a built-in `popcount()` method that returns the number of non-zero bits in the integer. Here's an example implementation:

```python
def count_nonzero_bits(n):
    return n.popcount()
```
