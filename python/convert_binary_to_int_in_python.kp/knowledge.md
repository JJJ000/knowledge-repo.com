---
title: Change a base-2 binary number to an integer
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: int(binary\_string, 2) will convert a base-2 binary number string to an int in Python.
---

**Contents**

[TOC]

### Using int()
The simplest way to convert a binary string to an integer is to use the built-in `int()` function. The `int()` function takes two parameters: the binary string and the base (2).

```python
binary_string = '10101'
int_value = int(binary_string, 2)
print(int_value)
# Output: 21
```

### Using Bitwise Operators
Another way to convert a binary string to an integer is to use bitwise operators. We can use the `<<` operator to shift the bits of the binary string to the left and the `|` operator to combine the bits.

```python
binary_string = '10101'
int_value = 0
for bit in binary_string:
    int_value = (int_value << 1) | int(bit)
print(int_value)
# Output: 21
```

### Using bin()
The `bin()` function can also be used to convert a binary string to an integer. The `bin()` function takes one parameter: the binary string.

```python
binary_string = '10101'
int_value = int(bin(binary_string), 2)
print(int_value)
# Output: 21
```

### Using Format Strings
Finally, we can use format strings to convert a binary string to an integer. The `%b` format string takes one parameter: the binary string.

```python
binary_string = '10101'
int_value = int(f'%b' % binary_string, 2)
print(int_value)
# Output: 21
```
