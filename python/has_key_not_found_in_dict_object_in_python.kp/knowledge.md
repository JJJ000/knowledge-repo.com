---
title: The 'dict' object does not possess the attribute 'has_key'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The `has\_key` method was removed in Python 3, and in Python 2.7 it is recommended to use `in` instead.
---

**Contents**

[TOC]

Introduction
------------
One of the most common errors you may face while working with dictionaries in Python is `'dict' object has no attribute 'has_key'`. This error usually occurs when you try to use the `has_key()` method to check if a key exists in a dictionary. In this article, we will understand why this error occurs and learn some ways to fix it.

Explanation of the Error Message
-------------------------------
In Python 3, the `has_key()` method is removed from the `dict` object. This is because the `in` keyword is a better and more Pythonic way to check if a key exists in a dictionary. Therefore, if you try to use the `has_key()` method in Python 3, you will get the following error message:

```
AttributeError: 'dict' object has no attribute 'has_key'
```

This error message simply means that the `has_key()` method is not a valid method in Python 3.

Ways to Fix the Error
---------------------
Here are two ways to fix the `'dict' object has no attribute 'has_key'` error:

### 1. Use the `in` Keyword
In Python, you can check if a key exists in a dictionary using the `in` keyword. Here is an example:

```python
my_dict = {'name': 'John', 'age': 25}
if 'name' in my_dict:
    print('name is a key in my_dict')
```

In this example, we use the `in` keyword to check if the key `'name'` exists in the `my_dict` dictionary. If it exists, we print a message saying that `'name'` is a key in `my_dict`.

### 2. Use the `get()` Method
In Python, you can also use the `get()` method to check if a key exists in a dictionary. Here is an example:

```python
my_dict = {'name': 'John', 'age': 25}
if my_dict.get('name') is not None:
    print('name is a key in my_dict')
```

In this example, we use the `get()` method to retrieve the value associated with the key `'name'`. If the key exists, `get()` will return its value. If the key does not exist, `get()` will return `None`. Therefore, we check if the return value of `get()` is not `None` to determine if the key exists in the dictionary. If it exists, we print a message saying that `'name'` is a key in `my_dict`.

Conclusion
----------
The `has_key()` method is not a valid method in Python 3. If you try to use it, you will get the `'dict' object has no attribute 'has_key'` error. To fix this error, you can use the `in` keyword or the `get()` method to check if a key exists in a dictionary. These are better and more Pythonic ways to achieve the same result.
