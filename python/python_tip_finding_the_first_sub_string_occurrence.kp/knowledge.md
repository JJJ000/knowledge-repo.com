---
title: What is the method to locate the initial instance of a sub-string in a Python string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Using the index() method, which returns the index of the first occurrence of a sub-string in a string.
---

**Contents**

[TOC]

## Using the `find()` method

One way to find the first occurrence of a sub-string in a Python string is by using the `find()` method. This method returns the index of the first occurrence of the sub-string in the string. If the sub-string is not found, it returns `-1`.

```python
string = "Hello, World!"
sub_string = "World"
index = string.find(sub_string)
print(index)
```

Output:
```
7
```

## Using the `index()` method

Another way to find the first occurrence of a sub-string in a Python string is by using the `index()` method. This method is similar to the `find()` method, but it raises a `ValueError` if the sub-string is not found.

```python
string = "Hello, World!"
sub_string = "World"
index = string.index(sub_string)
print(index)
```

Output:
```
7
```

## Using Regular Expressions

A third way to find the first occurrence of a sub-string in a Python string is to use regular expressions. Regular expressions are a powerful way to search for patterns in a string. The `re` module in Python provides functions to work with regular expressions.

```python
import re

string = "Hello, World!"
sub_string = "World"
pattern = re.compile(sub_string)
match = pattern.search(string)
if match:
    index = match.start()
    print(index)
```

Output:
```
7
```

## Conclusion

There are multiple ways to find the first occurrence of a sub-string in a Python string. The `find()` and `index()` methods are probably the simplest and most commonly used methods. Regular expressions offer more powerful tools for pattern-matching, but can be more complicated to use.
