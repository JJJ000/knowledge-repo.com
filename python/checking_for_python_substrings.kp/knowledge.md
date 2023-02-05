---
title: Is there a way to determine if a particular Python string is a part of another string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `in` operator to check if a given Python string is a substring of another one.
---

**Contents**

[TOC]

1. Using `in` Operator
--------------------------------
The `in` operator can be used to check if a string is a substring of another one. The syntax for this is as follows:

```python
substring in string
```

Where `substring` is the substring to be checked and `string` is the string to be checked against.

If the substring is a part of the string, the expression evaluates to `True`, otherwise it evaluates to `False`.

For example:

```python
"Python" in "Python is a programming language"
```

This expression evaluates to `True`.

2. Using `find()` Method
--------------------------------
The `find()` method can also be used to check if a string is a substring of another one. The syntax for this is as follows:

```python
string.find(substring)
```

Where `substring` is the substring to be checked and `string` is the string to be checked against.

If the substring is a part of the string, the expression evaluates to the index of the first occurrence of the substring in the string, otherwise it evaluates to `-1`.

For example:

```python
"Python is a programming language".find("Python")
```

This expression evaluates to `0`, which is the index of the first occurrence of `Python` in the string.

3. Using `index()` Method
--------------------------------
The `index()` method can also be used to check if a string is a substring of another one. The syntax for this is as follows:

```python
string.index(substring)
```

Where `substring` is the substring to be checked and `string` is the string to be checked against.

If the substring is a part of the string, the expression evaluates to the index of the first occurrence of the substring in the string, otherwise it raises a `ValueError` exception.

For example:

```python
"Python is a programming language".index("Python")
```

This expression evaluates to `0`, which is the index of the first occurrence of `Python` in the string.
