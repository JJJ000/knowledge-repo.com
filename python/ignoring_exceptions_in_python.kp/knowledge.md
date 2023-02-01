---
title: How to bypass an exception and continue in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use `try/except` blocks to catch exceptions and ignore them by using the `pass` keyword.
---

**Contents**

[TOC]

#Solution 1: Try/Except

The try/except statement is a basic way to handle exceptions in Python. The try block contains code that may throw an exception, and the except block contains code that will handle the exception.

```python
try:
   # code that may throw an exception
except:
   # code that will handle the exception
```

#Solution 2: Ignoring Exceptions

The "pass" statement can be used to ignore exceptions and continue execution.

```python
try:
   # code that may throw an exception
except:
   # ignore the exception
   pass
```

#Solution 3: Use a Logger

Using a logger is another way to handle exceptions in Python. A logger can be used to log messages and exceptions in a log file.

```python
import logging

try:
   # code that may throw an exception
except Exception as e:
   # log the exception
   logging.exception(e)
```

#Solution 4: Use a Context Manager

Using a context manager is another way to ignore exceptions and continue execution. A context manager is used to manage resources that need to be closed or cleaned up after the execution of a block of code.

```python
with contextlib.suppress(Exception):
   # code that may throw an exception
```
