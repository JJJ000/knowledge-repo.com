---
title: What is the method for determining if a string is empty?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To check if a string is empty in Python, use the built-in function len() to check the length of the string.
---

**Contents**

[TOC]

1. Using `len()` Function 

The `len()` function is used to find the length of a string. If the length of the string is 0, it means the string is empty.

```python
if len(string) == 0:
    print("String is empty")
```

2. Using `not` Operator

The `not` operator can be used to check if the string is empty.

```python
if not string:
    print("String is empty")
```

3. Using `==` Operator

The `==` operator can be used to check if the string is empty.

```python
if string == "":
    print("String is empty")
```

4. Using `is` Operator

The `is` operator can be used to check if the string is empty.

```python
if string is "":
    print("String is empty")
```
