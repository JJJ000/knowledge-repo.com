---
title: Why does Python 3 process the expression "10**100 in range(10**100)" so quickly?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Python 3 uses an optimized `range` implementation which stores the `range` as a sequence of integers, allowing it to quickly check if a given number is within the `range`.
---

**Contents**

[TOC]

### Range() Function
The `range()` function in Python 3 is an efficient way to generate a sequence of numbers. It is faster than other methods, such as looping through a list of numbers, because it only needs to process the start and end points of the range. This makes it much faster for large ranges. 

### Integer Representation
In Python 3, integers are represented using an efficient binary format. This allows for quick comparison of two integers, as the computer only needs to compare the binary values. This is why the expression "50000000000000000 in range(50000000000000001)" is so fast, as the computer only needs to compare the binary values of the two numbers. 

### Big Integer Support
Python 3 also supports large integers, known as "big integers". These integers are stored in a different format than regular integers, which allows for quick comparison of two large numbers. This is why the expression "50000000000000000 in range(50000000000000001)" is so fast in Python 3, as the computer only needs to compare the big integer values of the two numbers. 

### Optimizations
Python 3 also includes optimizations that make `range()` function faster. These optimizations include caching of range values, so that the same range doesn't need to be calculated multiple times, and optimizations to the `range()` function itself, which make it faster to generate a sequence of numbers.
