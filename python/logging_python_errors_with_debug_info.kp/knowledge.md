---
title: What is the process for logging a Python error with debug information?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can log a Python error with debug information by using the logging module to capture the error and its stack trace.
---

**Contents**

[TOC]

# Logging the Error

1. Use the `logging` module in Python to log the error.

2. Set the logging level to `logging.ERROR` to ensure only errors are logged.

3. Use `logging.error()` to log the error message along with any other relevant information such as the line number, file name, traceback, etc.

# Adding Debug Information

1. Use the `logging` module's `logging.debug()` method to log additional debug information.

2. Set the logging level to `logging.DEBUG` to ensure all debug messages are logged.

3. Include relevant information such as the line number, file name, traceback, etc.

4. Use the `logging.exception()` method to log the full traceback of the error.
