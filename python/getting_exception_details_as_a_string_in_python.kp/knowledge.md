---
title: Obtain the description of the exception and the stack trace that caused the exception, both as a single string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The exception description and stack trace can be obtained as a string by using the traceback.format\_exc() method.
---

**Contents**

[TOC]

# Exception Description
The exception description is a brief description of what caused the exception. It usually provides an indication of what type of error occurred and may include information about the line of code that caused the exception.

# Stack Trace
The stack trace is a list of function calls that were executed when the exception was thrown. It shows the exact order of the functions that were called, along with the line numbers where the exception was thrown. This information can be used to pinpoint the exact line of code that caused the exception.

# Combining Exception Description and Stack Trace
The exception description and stack trace can be combined into a single string by using the Python traceback module. This module provides a function called format_exception, which takes an exception object and returns a string containing both the exception description and the stack trace.
