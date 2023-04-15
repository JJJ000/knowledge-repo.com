---
title: How do I handle multiple exceptions in a single except clause
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can catch multiple exceptions in one line of a Python except block using parentheses, like `except (Exception1, Exception2) as e:`.
---

**Contents**

[TOC]

### Syntax

```python
try:
   # do something
except (Exception1[, Exception2[,...ExceptionN]]]):
   # handle exceptions
```

### Explanation

The syntax above allows us to catch multiple exceptions in one line (except block). The exceptions are specified in parentheses and are separated by a comma. If an exception occurs, the corresponding block is executed.

### Example

For example, the following code catches both TypeError and ValueError exceptions:

```python
try:
   # do something
except (TypeError, ValueError):
   # handle exceptions
```
