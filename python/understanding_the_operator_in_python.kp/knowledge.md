---
title: Can you explain what the += operator does?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The += operator in Python performs an addition operation on the variable on the left-hand side and the value on the right-hand side, and then assigns the result to the left-hand side variable.
---

**Contents**

[TOC]

## Addition
The `+=` operator in Python is used to perform an addition operation and assign the result to a variable. It adds the right operand to the left operand and assigns the result to the left operand. This is also called an "in-place addition" operation.

Syntax:
```
a += b
```

Explanation:
```
a = a + b
```

Example:
```
x = 5
x += 3   # adds 3 to x and assigns the result to x
print(x) # output: 8
```

## Concatenation
The `+=` operator can also be used to concatenate strings or lists. It concatenates the right operand to the left operand and assigns the result to the left operand.

Syntax:
```
a += b
```

Explanation:
```
a = a + b
```

Example:
```
s = 'Hello '
s += 'World'   # concatenates 'World' to s and assigns the result to s
print(s)       # output: 'Hello World'

lst = [1, 2, 3]
lst += [4, 5]   # concatenates [4, 5] to lst and assigns the result to lst
print(lst)      # output: [1, 2, 3, 4, 5]
```

## Other Operators
The `+=` operator can also be used with other arithmetic operators such as subtraction, multiplication, division, modulus, bitwise operation, etc. 

Syntax:
```
a <operator>= b
```

Explanation:
```
a = a <operator> b
```

Example:
```
x = 5
x -= 3   # subtracts 3 from x and assigns the result to x
print(x) # output: 2

x = 5
x *= 3   # multiplies 3 with x and assigns the result to x
print(x) # output: 15

x = 5
x //= 3   # divides x by 3, discards the remainder, and assigns the result to x
print(x)  # output: 1

x = 5
x %= 3   # finds the remainder when x is divided by 3 and assigns the result to x
print(x) # output: 2

x = 5
x **= 3   # raises x to the power of 3 and assigns the result to x
print(x)  # output: 125
```
