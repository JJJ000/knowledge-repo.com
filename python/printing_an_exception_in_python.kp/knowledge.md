---
title: What is the syntax for printing an exception in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `print()` function to print an exception in Python.
---

**Contents**

[TOC]

# Using Print Statement

Printing an exception in Python is relatively straightforward. To do so, simply use the print statement, followed by the exception object that you want to print.

For example:

```python
try:
    # some code
except Exception as e:
    print(e)
```

# Using Logging

Another way to print an exception in Python is to use the logging module. This module allows you to log messages to a file or other output stream.

To use the logging module, simply import it, create a Logger object, and call the exception() method on the Logger object.

For example:

```python
import logging

logger = logging.getLogger(__name__)

try:
    # some code
except Exception as e:
    logger.exception(e)
```
