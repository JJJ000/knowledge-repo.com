---
title: What is the correct way to obtain the exception message in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To get the exception message in Python, use the `str()` function or the `args` attribute of the exception object.
---

**Contents**

[TOC]

1. Introduction
Python is a high-level programming language that provides many built-in error handling features. When an error occurs during runtime, an exception object is created that contains information about the error. In this guide, we will discuss how to properly retrieve the exception message in Python.

2. Using try/except Blocks to Catch Exceptions
The most common way to handle exceptions in Python is by using try/except blocks. Here's an example:

```
try:
    # some code that may raise an exception
except Exception as e:
    print(e)
```

In this example, we catch any exception that gets raised by the code in the try block. The `as` keyword is used to assign the exception object to the `e` variable. We then print the value of the exception, which is the exception message.

3. Using the traceback Module to Retrieve More Information
The traceback module provides more information about the exception that occurred. Here's an example:

```
import traceback

try:
    # some code that may raise an exception
except Exception as e:
    print(traceback.format_exc())
```

In this example, we import the traceback module and use the `format_exc()` function to print a traceback of the exception. This includes the exception type, the stack trace, and the exception message.

4. Raising Custom Exceptions with Custom Messages
In some cases, it may be necessary to raise custom exceptions with custom error messages. Here's an example:

```
class CustomException(Exception):
    pass

try:
    raise CustomException("This is a custom exception message.")
except CustomException as e:
    print(e)
```

In this example, we define a custom exception class called `CustomException`. We raise an instance of this exception class with a custom error message. We then catch the exception and print the value of the exception, which is the custom error message.

5. Conclusion
Retrieving the exception message in Python is an important part of error handling. By using try/except blocks, the traceback module, and custom exception classes, you can effectively handle and communicate errors in your Python code.
