---
title: What is the syntax for using string.replace() in Python 3.x?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: String.replace() can be used to replace a specified substring in a string with another substring.
---

**Contents**

[TOC]

### Overview
String.replace() is a string method in Python 3.x that allows for a string to be replaced with another string. It takes two parameters, the old string and the new string, and returns a string with all occurrences of the old string replaced with the new string.

### Syntax
The syntax for string.replace() is as follows:

`string.replace(old, new[, count])`

Where `old` is the string to be replaced, `new` is the string to replace it with, and `count` is an optional parameter that specifies the maximum number of replacements to make.

### Examples

Here are some examples of using string.replace():

```
# Replace all occurrences of 'a' with 'b'
string = 'This is a string.'
string.replace('a', 'b')

# Output: 'This is b string.'
```

```
# Replace the first two occurrences of 'a' with 'b'
string = 'This is a string.'
string.replace('a', 'b', 2)

# Output: 'This is bb string.'
```

### Further Reading
For more information on string.replace() and other string methods, please refer to the official Python 3.x documentation [here](https://docs.python.org/3/library/stdtypes.html#string-methods).
