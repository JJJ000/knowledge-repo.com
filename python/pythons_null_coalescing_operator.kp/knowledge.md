---
title: What is the Python version of the c# null-coalescing operator?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Yes, the Python equivalent of the C# null-coalescing operator is the `or` operator.
---

**Contents**

[TOC]

## Using the `or` Operator
The Python equivalent of the C# null-coalescing operator is the `or` operator. This operator is used to return the first operand if it is not `None` or `False`, otherwise it returns the second operand. 

For example:
```python
x = None
y = 10

z = x or y

print(z)  # 10
```

## Using the `get()` Method
The `get()` method of the `dict` class can also be used to achieve the same result. This method takes two arguments, the first one being the key to look for and the second one being the value to return if the key is not found. 

For example:
```python
d = {'a': 1, 'b': 2}

x = d.get('c', 10)

print(x)  # 10
```

## Using the `is not None` Operator
The `is not None` operator can also be used to achieve the same result. This operator is used to check if a value is not `None` and return it, otherwise it returns the second operand. 

For example:
```python
x = None
y = 10

z = x if x is not None else y

print(z)  # 10
```
