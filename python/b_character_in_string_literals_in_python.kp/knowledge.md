---
title: What is the purpose of the 'b' character when placed before a string literal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `b` character in front of a string literal indicates that the string is a byte string, which is a sequence of bytes representing Unicode characters.
---

**Contents**

[TOC]

# Escape Character
The 'b' character is an escape character that is used to indicate that the following character should be interpreted as a literal character. This is helpful when a character has a special meaning in Python, such as a new line or tab.

# Raw Strings
The 'b' character can also be used to create a raw string literal. Raw strings are strings that are not interpreted by Python, which allows for the inclusion of characters that would otherwise be treated as special characters.

# Bypassing Syntax Errors
Finally, the 'b' character can be used to bypass syntax errors in Python. For example, if a string literal contains a single quote, the 'b' character can be used to indicate that the single quote should be treated as a literal character instead of being interpreted as the end of the string.
