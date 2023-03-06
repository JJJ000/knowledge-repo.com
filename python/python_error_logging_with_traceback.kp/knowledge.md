---
title: Record traceback for exceptions in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the traceback module in Python to log the exception with traceback.
---

**Contents**

[TOC]

## Overview

In this article, we will discuss how to log an exception with a traceback in Python. Exceptions are raised by the interpreter when an error occurs in the execution of Python code. In logging, it is a common practice to log exceptions and their tracebacks. A traceback is a stack trace of the exception and contains details about the line on which the exception occurred, the current stack frame, and the call stack. Logging exceptions with tracebacks can help developers debug errors and troubleshoot issues in their code.

## Catching and Logging Exceptions

When an exception is raised in Python, you can catch it using a `try` and `except` block. Within the `except` block, you can log the exception using a logging library such as `logging`. Here is an example of how to catch and log an exception with a traceback:

```python
import logging

try:
    # some code that may raise an exception
except Exception as e:
    logging.error("An exception occurred: {}".format(str(e)), exc_info=True)
```

In this example, we are catching all exceptions using the `Exception` base class. We pass the `exc_info=True` parameter to the logging function so that the exception traceback is also logged.

## Custom Exception Handlers

Python provides a way to define custom exception handlers using the `sys.excepthook()` function. This function can be used to replace the default exception handler and define a custom handler that logs the exception with a traceback. Here is an example of a custom exception handler that logs exceptions to a file:

```python
import logging
import sys

def log_exception(exctype, value, tb):
    logging.error("An exception occurred: {}".format(str(value)), exc_info=(exctype, value, tb))

sys.excepthook = log_exception
```

In this example, we define a custom function `log_exception()` that takes the exception type, value, and traceback as parameters. The function uses the `logging` library to log the exception with the traceback. We then set the `sys.excepthook()` function to our custom function so that it is used as the default exception handler.

## Using Decorators

Python provides a way to use decorators to log exceptions with tracebacks. A decorator is a function that takes another function as input and adds functionality to it. Here is an example of a decorator that logs exceptions:

```python

import logging

def log_exceptions(func):
    def wrapper(*args, **kwargs):
        try:
            return func(*args, **kwargs)
        except Exception as e:
            logging.error("An exception occurred: {}".format(str(e)), exc_info=True)
    return wrapper

@log_exceptions
def some_function():
    # some code that may raise an exception
```

In this example, we define a decorator function `log_exceptions()`. This function takes another function as input and returns a new function that logs exceptions. The wrapper function is defined inside the `log_exceptions()` function and wraps the original function. When the `some_function()` function is called, it will be wrapped by the `log_exceptions()` function, which will catch any exceptions and log them with a traceback.

## Conclusion

In this article, we discussed how to log exceptions with tracebacks in Python. We covered three methods for logging exceptions: catching and logging exceptions using a `try` and `except` block, defining a custom exception handler using the `sys.excepthook()` function, and using decorators to log exceptions. Logging exceptions with tracebacks can help developers debug errors and troubleshoot issues in their code.
