---
title: How can we rephrase "inner exception" (with traceback) in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Inner exception in Python refers to the original error that occurred before the current error, and it can be accessed through the `args` attribute of the current exception object.
---

**Contents**

[TOC]

Section 1: Introduction to "Inner exception"
When an error occurs in a try block in Python, the code jumps immediately to the except block. Sometimes, however, the error can occur while trying to handle the error itself. This is where "inner exceptions" come in. An inner exception is a secondary exception that occurs while handling a primary exception.

Section 2: How to access Inner Exception in Python?
To access the inner exception in Python, we need to use the __cause__ or __context__ built-in attributes of an exception object. The __cause__ attribute returns the exception that caused the primary exception, while the __context__ attribute returns the context in which the primary exception occurred.

Section 3: Example of using inner exception in Python
```
import traceback

try:
    # some code that may raise an exception
except Exception as e:
    try:
        # code to handle the exception
    except Exception as inner_e:
        print("Inner exception occurred:", traceback.format_exc(inner_e))
```

In this example, we have a primary try block that may raise an exception. If an exception is raised, we have a secondary try block to handle the exception. If an inner exception occurs while handling the primary exception, we catch it and print out a traceback message that includes the inner exception.

Section 4: Conclusion
Inner exceptions are an advanced feature of Python exception handling that allow us to handle nested exceptions more gracefully. By utilizing the __cause__ and __context__ attributes of an exception object, we can identify the root cause of an exception and take appropriate action.
