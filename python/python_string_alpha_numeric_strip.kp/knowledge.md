---
title: Removing all non-alphanumeric characters from a string in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the `re` module`s `sub` function to replace all non-alphanumeric characters with an empty string.
---

**Contents**

[TOC]

### Using Regular Expressions
Python's `re` module provides regular expression matching operations similar to those found in Perl.

Using `re.sub()`, we can replace all non-alphanumeric characters with an empty string:

```python
import re

s = 'Hello, World!'
s = re.sub(r'[^\w]', '', s)
print(s) # Output: HelloWorld
```

### Using str.translate()
Python's `str.translate()` method can be used to remove all non-alphanumeric characters from a string.

The `str.maketrans()` method can be used to create a translation table. This table maps each character in the input string to its corresponding character in the output string.

```python
import string

s = 'Hello, World!'
table = str.maketrans('', '', string.punctuation)
s = s.translate(table)
print(s) # Output: HelloWorld
```

### Using List Comprehension
We can also use list comprehension to filter out all non-alphanumeric characters from a string.

```python
s = 'Hello, World!'
s = ''.join([c for c in s if c.isalnum()])
print(s) # Output: HelloWorld
```

### Using a For Loop
We can also use a for loop to iterate over the characters in the string and build a new string without the non-alphanumeric characters.

```python
s = 'Hello, World!'
s_new = ''
for c in s:
    if c.isalnum():
        s_new += c
print(s_new) # Output: HelloWorld
```
