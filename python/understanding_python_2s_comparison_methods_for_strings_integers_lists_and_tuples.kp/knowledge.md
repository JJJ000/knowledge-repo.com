---
title: In what manner does Python 2 differentiate string and integer comparisons? what is the rationale behind placing lists above numbers and tuples above lists in the comparison hierarchy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Python 2 compares string and int based on their Unicode value, while the comparisons of lists and tuples are based on lexicographical order and length.
---

**Contents**

[TOC]

## Comparison of Strings and Integers in Python 2

Comparing strings and integers in Python 2 involves several considerations. In Python 2, the `cmp()` function is used for comparing the values of two objects, regardless of their types. However, the `cmp()` function is removed in Python 3 as it is not required anymore because the `<`, `>`, `<=`, and `>=` operators work for objects of different types as well.

It is worth noting that when `cmp()` is used to compare a string and an integer in Python 2, Python compares their corresponding ASCII codes instead of their actual values. Therefore, if we use the `cmp()` function to compare the string "2" and the integer 2, it will return a non-zero value because "2" has a higher ASCII code than 2. Hence, it is recommended to use the `int()` function to convert the string to an integer before performing any arithmetic operations.

```python
>>> cmp("2", 2)
1
>>> cmp("2", int(2))
0
>>> cmp("apple", 1)
1
```

## Comparison of Lists and Numbers

When comparing a list to a number, Python compares their types first before their values. Since the list and integer have different types, Python considers the list greater than the integer.

```python
>>> [1, 2, 3] > 2
True
```

## Comparison of Tuples and Lists

When comparing a tuple to a list, Python again compares their types first before their values. Since the tuple and list have different types, Python considers the tuple greater than the list.

```python
>>> (1, 2, 3) > [1, 2, 3]
True
```

It is worth noting that comparing objects of different types is not recommended because it can lead to unexpected outcomes. Therefore, it is recommended to compare objects of the same type for consistency and predictability in your code.
