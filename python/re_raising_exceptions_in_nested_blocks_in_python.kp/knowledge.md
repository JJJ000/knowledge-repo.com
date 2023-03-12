---
title: What is the method for re-raising an exception within try/except blocks that are nested?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can simply use the `raise` statement followed by the caught exception within the inner `except` block.
---

**Contents**

[TOC]

## Using `raise` statement

One common way to re-raise an exception in nested try/except blocks in Python is to use the `raise` statement without any arguments. This will re-raise the exception that was caught in the innermost try block, allowing it to be caught by an outer except block or to propagate up the call stack to the top-level error handler (such as the Python interpreter).

```python
try:
    # some code that raises an exception
except SomeException:
    try:
        # handle the exception in some way
    except AnotherException:
        # handle the exception in another way
        raise  # re-raise the original exception
```

In this example, if the first except block catches an exception of type `SomeException`, the second try block can handle it in some way. If the handling code then raises an exception of type `AnotherException`, the third except block can handle it in another way, but then re-raises the original `SomeException` by using the `raise` statement without any arguments.

## Using `raise` with modified message

Sometimes it can be useful to modify the error message before re-raising an exception. This can provide additional context or information about the error that was caught and is being propagated up the call stack. To do this, we can pass a new exception object with a modified error message as the argument to the `raise` statement.

```python
try:
    # some code that raises an exception
except SomeException as e:
    try:
        # handle the exception in some way
    except AnotherException:
        # handle the exception in another way
        new_message = f"{e} could not be processed"
        raise SomeException(new_message) from e
```

In this example, if the first except block catches an exception of type `SomeException`, the second try block can handle it in some way. If the handling code then raises an exception of type `AnotherException`, the third except block can handle it in another way, but then re-raises a new `SomeException` object with a modified error message.

## Using `sys.exc_info`

Another approach to re-raising an exception in Python is to use the `sys.exc_info` function to obtain information about the current exception and then use the `raise` statement with that information to re-raise it. This allows us to capture more detailed information about the exception, such as its type, value, and traceback.

```python
import sys

try:
    # some code that raises an exception
except SomeException:
    try:
        # handle the exception in some way
    except AnotherException:
        # handle the exception in another way
        exc_type, exc_value, exc_tb = sys.exc_info()
        raise exc_type(exc_value).with_traceback(exc_tb)
```

In this example, if the first except block catches an exception of type `SomeException`, the second try block can handle it in some way. If the handling code then raises an exception of type `AnotherException`, the third except block can handle it in another way, but then re-raises the original exception with its original traceback information using `sys.exc_info`.
