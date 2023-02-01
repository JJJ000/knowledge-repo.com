---
title: What is the process for locating all instances of a particular string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the str.find() or str.index() methods to find all occurrences of a substring in Python.
---

**Contents**

[TOC]

## Using `find()`

The `find()` method can be used to find the index of the first occurrence of a substring in a string. This method returns the index of the substring if found, otherwise it returns -1.

Example:
```
str = "Python is an interpreted, high-level, general-purpose programming language"

# find first occurrence of "Python"
result = str.find("Python")

# print result
print("Substring found at index:", result)
```

Output:
```
Substring found at index: 0
```

## Using `index()`

The `index()` method is similar to the `find()` method, but it raises an exception if the substring is not found.

Example:
```
str = "Python is an interpreted, high-level, general-purpose programming language"

# find first occurrence of "Python"
result = str.index("Python")

# print result
print("Substring found at index:", result)
```

Output:
```
Substring found at index: 0
```

## Using `count()`

The `count()` method can be used to count the number of times a substring occurs in a string.

Example:
```
str = "Python is an interpreted, high-level, general-purpose programming language"

# count occurrences of "Python"
result = str.count("Python")

# print result
print("Number of occurrences of substring:", result)
```

Output:
```
Number of occurrences of substring: 1
```

## Using `re.findall()`

The `re.findall()` method can be used to find all the occurrences of a substring in a string.

Example:
```
import re

str = "Python is an interpreted, high-level, general-purpose programming language"

# find all occurrences of "Python"
result = re.findall("Python", str)

# print result
print("Number of occurrences of substring:", len(result))
```

Output:
```
Number of occurrences of substring: 1
```
