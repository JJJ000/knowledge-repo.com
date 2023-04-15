---
title: Can you provide extra details to an exception?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `raise` statement with an instance of an exception class and pass additional information to the constructor of the exception class.
---

**Contents**

[TOC]

## Overview

Exceptions are raised when an error occurs during the execution of a Python program. Exception handling is an important aspect of writing robust and reliable Python code. In some cases, it may be necessary to add information to an exception to provide more context about the error. In this article, we will explore how to add information to a Python exception.

## Using the `raise` statement

When an exception is raised in Python, it can be caught by a `try/except` block. The `raise` statement can be used to raise an exception with an optional message. To add information to an exception, we can include additional information in this message.

```python
try:
    # some code that might raise an exception
except Exception as e:
    raise Exception("Additional information: " + str(e))
```

In this example, we catch an exception and then raise a new exception with additional information. The original exception is included in the message using the `str()` function.

## Creating custom exceptions

In some cases, it may be useful to create a custom exception with specific information. We can create a custom exception class by subclassing the built-in `Exception` class.

```python
class CustomException(Exception):
    def __init__(self, message, extra_info):
        super().__init__(message)
        self.extra_info = extra_info
```

In this example, we define a custom exception class that takes a message and extra information as arguments. The `__init__` method of the class calls the `__init__` method of the base class and then stores the extra information as an instance variable.

We can then raise an instance of this custom exception in our code:

```python
try:
    # some code that might raise a custom exception
except CustomException as e:
    raise CustomException(e.message, "Additional information")
```

In this example, we catch a custom exception and then raise a new instance of the custom exception with additional information.

## Using the `args` attribute

All exceptions in Python have an `args` attribute, which is a tuple of arguments that were passed to the constructor of the exception. We can add additional information to this tuple by constructing a new tuple with the original arguments and additional information.

```python
try:
    # some code that might raise an exception
except Exception as e:
    new_args = e.args + ("Additional information",)
    raise type(e)(*new_args)
```

In this example, we catch an exception and then construct a new tuple with the original arguments and additional information. We then raise a new instance of the same type of exception with the new tuple as the arguments.

## Conclusion

Adding information to a Python exception can be useful for providing more context about an error. There are several ways to add information to an exception, including using the `raise` statement, creating custom exceptions, and modifying the `args` attribute. By adding informative error messages, we can make it easier to debug and fix problems in our Python programs.
