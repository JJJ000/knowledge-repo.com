---
title: What is the meaning of adding the letter "r" before a string literal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Preceding a string literal with `r` in Python means that the string should be treated as a `raw string` and any escape sequences should be ignored.
---

**Contents**

[TOC]

# Raw String Literal in Python

In Python, a raw string literal is a string that is prefixed with an 'r' or 'R' character. The raw string literal is used to indicate that the string should be treated as a raw string and all escape characters should be ignored.

# Escape Characters in Python Strings

In Python, escape characters are special characters that are used to represent certain characters in a string. For example, the escape character '\n' is used to represent a new line character, and the escape character '\t' is used to represent a tab character.

# Raw String Literal and Escape Characters

The use of a raw string literal in Python means that all escape characters are ignored. This is useful when working with regular expressions, file paths, and other cases where escape characters may cause issues if not properly handled.

# Example of Raw String Literal in Python

Here is an example of using a raw string literal in Python:

```
path = r'C:\Users\MyUser\Documents\file.txt'
```

In this example, the 'r' character indicates that the string should be treated as a raw string, and all escape characters should be ignored. This is useful when working with file paths on a Windows machine, where the backslash character is used as the directory separator.
