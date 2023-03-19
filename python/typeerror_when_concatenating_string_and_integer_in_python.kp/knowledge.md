---
title: The error message "typeerror cannot concatenate 'str' and 'int' objects" indicates that it is not possible to merge a string and an integer data type
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You cannot concatenate a string and integer directly, as they are different data types.
---

**Contents**

[TOC]

Section 1: Overview
-------------------

The `TypeError: cannot concatenate 'str' and 'int' objects` is a common error that occurs in Python. It indicates that there is an invalid operation being performed on objects of two different data types. In this case, the error occurs when trying to concatenate or add a string and an integer.

Section 2: Concatenating strings and integers
--------------------------------------------

In Python, the `+` operator is used for both addition and concatenation. If both operands are of the same data type, the operator performs the relevant operation. However, if the operands are of different types, Python tries to convert one of them to the other type.

When concatenating a string and an integer, Python can convert the integer to a string and then concatenate the two strings. However, if the integer is not explicitly converted to a string, it remains an integer, which causes the `TypeError` to be raised.

Here's an example:

```
str_value = 'hello'
int_value = 5
result = str_value + int_value
```

In this case, `str_value` is a string and `int_value` is an integer. Attempting to concatenate them with the `+` operator causes Python to raise a `TypeError`.

Section 3: How to fix the TypeError
----------------------------------

To fix the `TypeError: cannot concatenate 'str' and 'int' objects`, we need to ensure that both operands are of the same data type. In the case of concatenating a string and an integer, we can explicitly convert the integer to a string using the `str()` function.

Here's an updated example:

```
str_value = 'hello'
int_value = 5
result = str_value + str(int_value)
```

Here, `int_value` is converted to a string using the `str()` function before concatenating it with `str_value`.

Section 4: Conclusion
---------------------

In summary, the `TypeError: cannot concatenate 'str' and 'int' objects` occurs when trying to concatenate a string and an integer without converting the integer to a string first. To fix the error, we can convert the integer to a string using the `str()` function.
