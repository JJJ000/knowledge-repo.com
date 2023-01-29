---
title: What is the syntax for printing to stderr in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `print` function with the `file` argument set to `sys.stderr`.
---

**Contents**

[TOC]

1. Using `sys.stderr`
--------------------------------
The `sys` module provides access to functions related to the interpreter and to the operating system. `sys.stderr` is an output stream similar to `sys.stdout` which is used for standard output. 

To print a message to `sys.stderr`, the `print()` function can be used with `sys.stderr` as the file argument:

```python
import sys

print("This is an error message", file=sys.stderr)
```

2. Using `logging`
--------------------------------
The `logging` module provides functions and classes which help in the creation of log messages. The `logging.error()` function can be used to print a message to `sys.stderr`:

```python
import logging

logging.error("This is an error message")
```

3. Using `sys.stderr.write()`
--------------------------------
The `sys.stderr.write()` method can be used to write a string to `sys.stderr`:

```python
import sys

sys.stderr.write("This is an error message\n")
```

4. Using `sys.exit()`
--------------------------------
The `sys` module also provides a `sys.exit()` function which can be used to terminate the program and print an error message to `sys.stderr`:

```python
import sys

sys.exit("This is an error message")
```
