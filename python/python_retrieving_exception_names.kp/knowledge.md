---
title: What is the way to obtain the name of a caught exception in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use `type(exception).\_\_name\_\_` to get the name of the caught exception in Python.
---

**Contents**

[TOC]

## Using type() and str()

One way to get the name of an exception that was caught in Python is to use the built-in `type()` function to get the type of the exception, and then convert that type to a string using the `str()` function. Here's an example:

```python
try:
    some_code_that_may_raise_an_exception()
except Exception as e:
    exception_type = type(e)
    exception_name = str(exception_type)
    print("Caught an exception of type:", exception_name)
```

In this example, we first catch any exception that may occur in `some_code_that_may_raise_an_exception()`. We then use the `as` keyword to give the caught exception a variable name (`e` in this case). We then use the `type()` function to get the type of the caught exception, which will be a subclass of the `Exception` class. Finally, we use the `str()` function to convert the type to a string, which will give us the name of the exception.


## Using __class__.__name__

Another way to get the name of an exception that was caught in Python is to use the `__class__` attribute of the caught exception, followed by the `__name__` attribute. Here's an example:

```python
try:
    some_code_that_may_raise_an_exception()
except Exception as e:
    exception_name = e.__class__.__name__
    print("Caught an exception of type:", exception_name)
```

In this example, we do essentially the same thing as before: catch any exception that may occur in `some_code_that_may_raise_an_exception()`, and give the caught exception a variable name (`e`). We then use the `__class__` attribute of the caught exception to get its type, and then use the `__name__` attribute to get the name of that type as a string. Finally, we print out the name of the exception.


## Using traceback.format_exc()

A third way to get the name of an exception that was caught in Python is to use the `traceback.format_exc()` function, which returns a string that includes the name of the exception along with a traceback of the error. Here's an example:

```python
import traceback

try:
    some_code_that_may_raise_an_exception()
except:
    exception_string = traceback.format_exc()
    print("Caught an exception:\n", exception_string)
```

In this example, we import the `traceback` module, which provides functions for printing and formatting traceback information. We then catch any exception that may occur in `some_code_that_may_raise_an_exception()` and create a string representation of the exception using `traceback.format_exc()`. This function returns a string that includes the name of the exception along with a traceback of the error. Finally, we print out the exception string. Note that we're using a bare `except:` here, which will catch any exception, including ones that are not subclasses of `Exception`. While this is generally not recommended, it can be useful for debugging purposes.
