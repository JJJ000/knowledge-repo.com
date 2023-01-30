---
title: Testing for non-null values in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Yes, the `not None` test in Python can be used to check if a value is not equal to None.
---

**Contents**

[TOC]

## Section 1: What is None?
None is a special constant in Python that represents the absence of a value or a null value. It is an object of its own datatype, the NoneType. It is not possible to create multiple None objects and can only have the value None.

## Section 2: How to Test for None
The easiest way to test for None is to use the `is` operator. This operator returns `True` if both the objects being compared are the same object. When comparing to None, it will return `True` if the object is None, and `False` if it is not.

## Section 3: Example

```python
x = None

if x is None:
    print('x is None')
else:
    print('x is not None')
```

This code will print `x is None`.

## Section 4: Other Ways to Test for None
It is also possible to test for None using the `==` operator, which will return `True` if both objects have the same value. However, this is not recommended since it is possible to have multiple objects with the same value but different identities. It is also possible to use the `not` operator to check if an object is not None.
