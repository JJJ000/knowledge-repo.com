---
title: In python, the operator represented by the tilde symbol is called
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The tilde operator in Python is a bitwise NOT operator that flips the bits of a number and adds 1 to the result.
---

**Contents**

[TOC]

Introduction to the tilde operator

In Python, the tilde operator is represented by the symbol "~". It is also known as the bitwise negation operator. The tilde operator takes the binary representation of a value and performs a bitwise NOT operation. This means that it flips all the bits in the binary representation of the value, including the sign bit for signed numbers. In this article, we will explore the various uses of the tilde operator in Python.

Using the tilde operator to perform bitwise negation

The most common use of the tilde operator in Python is to perform bitwise negation. This is done by placing the tilde operator before the value that needs to be negated. For example:

```
a = 10
b = ~a
print(b)  # Output: -11
```

In this example, the variable "a" has a binary representation of "1010". When we apply the tilde operator to it, we get the negation of this value, which is "0101". In decimal form, this is equal to "-11".

Using the tilde operator to perform bitwise NOT

In addition to bitwise negation, the tilde operator can also be used to perform a bitwise NOT operation on a value. This is done by first converting the value to its binary representation and then flipping all the bits. For example:

```
a = 10
b = bin(a)
c = ~a
d = bin(c)
print(b, d)  # Output: 0b1010 -0b1011
```

In this example, we first convert the value of "a" to its binary representation using the "bin()" function. This gives us the string "0b1010". We then use the tilde operator to perform a bitwise NOT operation on "a", which gives us the value "-11". Finally, we convert this value to its binary representation using the "bin()" function again. The result is the string "-0b1011".

Conclusion

In this article, we have explored the various uses of the tilde operator in Python. We have seen how it can be used to perform bitwise negation and bitwise NOT operations on values. The tilde operator is a powerful tool that can be used in a variety of contexts, such as working with binary data, performing bitwise arithmetic, and manipulating bit flags.
