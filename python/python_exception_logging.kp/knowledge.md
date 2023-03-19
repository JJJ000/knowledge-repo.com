---
title: Recording unexpected errors in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the logging module in Python to log uncaught exceptions, using the `exception` method to log the full traceback.
---

**Contents**

[TOC]

## Introduction
Uncaught exceptions in Python refer to errors that occur during the execution of a program but are not handled by an exception handler. When a Python program encounters an uncaught exception, it terminates immediately and prints the error message to the console. However, in some cases, you may want to log these exceptions to a file for further analysis. In this article, we will discuss how to log uncaught exceptions in Python.


## Using the sys module to log exceptions

One way to log uncaught exceptions in Python is to use the `sys` module's `excepthook()` function. This function is called whenever an uncaught exception occurs in a Python program. It takes three arguments: `etype`, `value`, and `traceback`. `etype` is the type of the exception that was raised, `value` is the exception instance that was raised, and `traceback` is a traceback object that contains information about the exception.

To use `excepthook()` to log uncaught exceptions, you can define a function that takes the same arguments as `excepthook()` and uses the `logging` module to write the exception information to a log file. For example:

```python
import sys
import logging

logging.basicConfig(filename='exceptions.log', level=logging.DEBUG)

def log_uncaught_exceptions(etype, value, traceback):
    logging.exception("Uncaught exception", exc_info=(etype, value, traceback))

sys.excepthook = log_uncaught_exceptions
```

In this example, we set the `basicConfig()` method of the `logging` module to write to a file called `exceptions.log` and set the logging level to the `DEBUG` level so that all uncaught exceptions are logged. We then define the `log_uncaught_exceptions()` function, which takes the three arguments of `excepthook()`. This function uses the `exception()` method of the `logging` module to log the exception information, including the traceback.


## Using the traceback module to log exceptions

Another way to log uncaught exceptions in Python is to use the `traceback` module to format the exception information and write it to a log file. This approach is similar to using `excepthook()`, but it gives you more control over the formatting and contents of the log file.

To use the `traceback` module to log uncaught exceptions, you can define a function that takes no arguments and uses the `traceback` module's `format_exception()` function to format the exception information into a string. You can then use the `logging` module to write this string to a log file. For example:

```python
import traceback
import logging

logging.basicConfig(filename='exceptions.log', level=logging.DEBUG)

def log_uncaught_exceptions():
    traceback_str = "".join(traceback.format_exception(*sys.exc_info()))
    logging.error("Uncaught exception:\n{}".format(traceback_str))

sys.excepthook = log_uncaught_exceptions
```

In this example, we still set up the `logging` module to write to a file called `exceptions.log` and set the logging level to the `DEBUG` level. We then define the `log_uncaught_exceptions()` function, which uses `traceback.format_exception()` to format the exception information into a string. This function then uses the `logging` module's `error()` method to write this string to the log file.


## Conclusion

In this article, we discussed two ways to log uncaught exceptions in Python: using the `sys` module's `excepthook()` function and the `traceback` module's `format_exception()` function. Both methods allow you to capture useful information about uncaught exceptions and store it in a file for further analysis. By logging uncaught exceptions, you can gain insights into the behavior of your program and identify and fix issues that may have gone unnoticed otherwise.
