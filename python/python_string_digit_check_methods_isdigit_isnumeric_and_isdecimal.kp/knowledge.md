---
title: Could you explain the distinctions between str.isdigit(), isnumeric(), and isdecimal() functions in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: str.isdigit() returns True if all characters in a string are digits, while isnumeric() and isdecimal() also include characters from other scripts and numerals not recognized as digits by str.isdigit().
---

**Contents**

[TOC]

# Introduction

Python provides three different methods that can be used to determine whether a string represents a numeric value, those are `str.isdigit()`, `str.isnumeric()` and `str.isdecimal()`. Although they all have a similar purpose, it is worth to know the differences between them to use the right one in each case, because they return different results based on the characters they consider as numeric.

# `str.isdigit()`

The `str.isdigit()` method returns `True` if all characters in the string are decimal digits (0 through 9). This means that it will not accept fractions, negative numbers, or any other kind of non-digit character.

```python
>>> "1234".isdigit()
True

>>> "3.14".isdigit()
False

>>> "-123".isdigit()
False

>>> "½".isdigit()
False
```

# `str.isnumeric()`

The `str.isnumeric()` method returns `True` if all characters in the string are numeric, including digits, fractions, subscripts, superscripts, and other numeric characters from Unicode.

```python
>>> "1234".isnumeric()
True

>>> "3.14".isnumeric()
False

>>> "-123".isnumeric()
False

>>> "½".isnumeric()
True

>>> "²".isnumeric()
True
```

# `str.isdecimal()`

The `str.isdecimal()` method returns `True` if all characters in the string are decimal numbers (0 through 9). It is similar to `str.isdigit()`, but it does not accept any other kind of numeric character, such as fractions or subscripts.

```python
>>> "1234".isdecimal()
True

>>> "3.14".isdecimal()
False

>>> "-123".isdecimal()
False

>>> "½".isdecimal()
False

>>> "²".isdecimal()
True
```

# Conclusion

In summary, `str.isdigit()` checks if all characters are decimal digits, `str.isnumeric()` checks if all characters are numeric, including more than just decimal digits, and `str.isdecimal()` checks if all characters are decimal numbers, but doesn't include more than just decimal digits. In general, if you need to check if a string represents a number, `str.isnumeric()` is usually the most versatile option, while `str.isdigit()` and `str.isdecimal()` are more limited in the kind of numeric characters they accept.
