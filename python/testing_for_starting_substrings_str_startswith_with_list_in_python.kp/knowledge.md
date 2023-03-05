---
title: Use a list of strings to test if a given string starts with any of them
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: In Python, you can use the str.startswith method with a tuple or list of strings to test for multiple prefixes.
---

**Contents**

[TOC]

Introduction
------------
The `str.startswith` method in Python is used to check if a given string starts with a specific character or sequence of characters. It returns a boolean value, `True` or `False`, depending on whether the string starts with the given character or sequence or not.

However, sometimes, we may want to check if a string starts with any of the several characters or sequences of characters. In such cases, we cannot use `str.startswith` directly, as it only works for a single string. This article explains one way to solve this problem.

Using str.startswith with a list of strings
--------------------------------------------
One way to use `str.startswith` with a list of strings is to loop through the list and use `str.startswith` on each string. Here is an example:

```python
strings = ['hello', 'world', 'python']
string_to_test = 'hello world'

for s in strings:
    if string_to_test.startswith(s):
        print(f"'{string_to_test}' starts with '{s}'")
```

This code will output:

```
'hello world' starts with 'hello'
```

We can see that the code successfully identifies that the target string starts with the first string in the list.

Using any() with a list of boolean values
------------------------------------------
Another, more concise, way to achieve the same result is to use the `any()` function with a list of boolean values. Here is the code:

```python
strings = ['hello', 'world', 'python']
string_to_test = 'hello world'

if any(string_to_test.startswith(s) for s in strings):
    print(f"'{string_to_test}' starts with one of {strings}")
```

This code will output:

```
'hello world' starts with one of ['hello', 'world', 'python']
```

We can see that the code successfully identifies that the target string starts with one of the strings in the list.

Conclusion
----------
In this article, we have seen how to use `str.startswith` with a list of strings in Python. We can either loop through the list and use `str.startswith` on each string, or we can use the `any()` function with a list of boolean values. The latter approach is more concise and elegant, and is recommended when we have a large number of strings to test for.
