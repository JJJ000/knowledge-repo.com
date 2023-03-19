---
title: Can you explain the functionality of the |= (ior) operator in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The |= (ior) operator in Python performs a bitwise OR operation on two values and assigns the result to the left operand.
---

**Contents**

[TOC]

# Understanding the |= (ior) Operator in Python

The `|=` (ior) operator in Python is a bitwise operator used for performing logical OR operation on two binary numbers. It takes the bitwise OR of two operands and assigns the result to the first operand.

## Syntax of the |= (ior) Operator in Python

The syntax of the |= operator in Python is as follows:

```python
a |= b
```

In the above syntax, `a` and `b` are numerical values where `a` is the variable that will be updated with the result of the OR operation.

## Example Usage of the |= (ior) Operator in Python

The following example demonstrates how the |= operator can be used to perform a bitwise OR operation on two binary numbers:

```python
x = 15    # binary value of 15 is 0b1111
y = 6     # binary value of 6 is 0b0110

x |= y    # perform a bitwise OR operation on x and y and assign the result to x

print(x)  # the output will be 15 since the binary value of 15 OR 6 is 0b1111
```

In the above example, we first initialized two variables `x` and `y` with binary values of 15 and 6 respectively. We then performed a bitwise OR operation on `x` and `y` using the `|=` operator and assigned the result to `x`. Finally, we printed the value of `x` which would be the result of the bitwise OR operation.

## Conclusion

The `|=` (ior) operator in Python is a powerful operator that can be used to perform a bitwise OR operation on two binary numbers and assign the result to the first operand. It is commonly used for manipulating binary values and can greatly simplify complex bitwise operations.
