---
title: In python, what is the meaning of >> and <<?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python, >> and << are bitwise shift operators used to shift the bits of a binary number to the left or right by the specified number of positions.
---

**Contents**

[TOC]

### Right-Shift Operator (>>)

The `>>` operator is known as the "right-shift operator" in Python. It takes two operands - the first one is the value to be shifted, while the second one specifies by how many bits to shift the value. 

When the right-shift operator is applied to an integer value `x` and a non-negative integer value `y`, the following steps are taken:

1. `x` is first converted to binary representation (i.e., a sequence of 0's and 1's).
2. `x` is then shifted to the right by `y` bits.
3. The bits that are shifted out on the right-hand side are discarded.
4. The bits that are shifted in on the left-hand side are set to 0.
5. The resulting binary sequence is converted back to an integer value.

For example, consider the following code snippet:

```python
x = 8
y = 2
result = x >> y
print(result)
```

In this case, the value of `x` is 8, which has a binary representation of `1000`. The value of `y` is 2, so we shift the binary representation of `x` 2 bits to the right:

```
    1 0 0 0  (8 in binary)
>>  _ _ 1 0  (shifted 2 bits to the right)
    -------
    0 0 1 0  (2 in binary)
```

The resulting binary sequence is `0010`, which represents the integer value 2. Therefore, the output of the code snippet is `2`.


### Left-Shift Operator (<<)

The `<<` operator is known as the "left-shift operator" in Python. It takes two operands - the first one is the value to be shifted, while the second one specifies by how many bits to shift the value. 

When the left-shift operator is applied to an integer value `x` and a non-negative integer value `y`, the following steps are taken:

1. `x` is first converted to binary representation (i.e., a sequence of 0's and 1's).
2. `x` is then shifted to the left by `y` bits.
3. The bits that are shifted out on the left-hand side are discarded.
4. The bits that are shifted in on the right-hand side are set to 0.
5. The resulting binary sequence is converted back to an integer value.

For example, consider the following code snippet:

```python
x = 2
y = 3
result = x << y
print(result)
```

In this case, the value of `x` is 2, which has a binary representation of `10`. The value of `y` is 3, so we shift the binary representation of `x` 3 bits to the left:

```
    1 0  (2 in binary)
<<  1 0 0 0  (shifted 3 bits to the left)
    -------
    1 0 0 0 0  (16 in binary)
```

The resulting binary sequence is `10000`, which represents the integer value 16. Therefore, the output of the code snippet is `16`.
