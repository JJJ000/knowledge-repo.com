---
title: What is the syntax for creating a line break (line continuation) in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Python, line breaks can be achieved by using the backslash (\) character at the end of a line.
---

**Contents**

[TOC]

# Using Backslash

The backslash character (\\) is used to indicate that the line should continue. This allows the programmer to write code on multiple lines, making it easier to read and debug.

For example:

```
x = 1 + 2 + \
    3 + 4
```

# Using Parentheses

Parentheses can also be used to indicate line continuation. This is useful when a statement is too long to fit on one line.

For example:

```
x = (1 + 2 +
     3 + 4)
```

# Using Triple Quotes

Triple quotes (''' or """) can also be used to indicate line continuation. This is useful when a statement is too long to fit on one line, or when the statement contains a quotation mark.

For example:

```
x = 'This is a very long statement that \
cannot fit on one line'
```

# Using Implicit Line Joining

In some cases, Python will implicitly join lines of code. This happens when an open parenthesis, square bracket, or curly brace is left open at the end of a line.

For example:

```
x = [1, 2,
     3, 4]
```
