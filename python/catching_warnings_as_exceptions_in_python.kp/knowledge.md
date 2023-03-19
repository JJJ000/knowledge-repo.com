---
title: How can warnings be caught in Python as if they were exceptions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can catch warnings as exceptions by using the warnings module and calling the warnings.filterwarnings() function with the `error` action.
---

**Contents**

[TOC]

### Overview

Python's `warnings` module provides a means of emitting warning messages that do not necessarily cause the program to abort as errors do. However, sometimes it is desirable to treat warnings as if they were exceptions, meaning that their occurrence will cause the program to raise an exception and halt execution. In this solution we show how to catch warnings as exceptions in Python using a simple function and demonstrate its usage on a sample code.


### Approach

To globally catch warnings as exceptions, we need to customize the behavior of the `warnings.showwarning` function, which is called by the ` warnings.warn` function whenever a warning is emitted. We can replace this function with our own that raises an exception whenever a warning is encountered. Here are the main steps involved:

1. Define our custom `showwarning` function that raises an exception of our choice whenever a warning is issued.
2. Set the custom `showwarning` function as the new `warnings.showwarning` function by calling the `warnings.showwarning = showwarning` statement.
3. Execute the code that may emit warnings.
4. Wrap the code in a `try`-`except` block that catches the exception raised by the custom `showwarning` function and handles it appropriately.


### Code

Here's an example of how to catch warnings as exceptions using the `showwarning` function:

```python
import warnings

def warn_to_exception(message, category, filename, lineno, file=None, line=None):
    raise category(message, (filename, lineno))

warnings.showwarning = warn_to_exception

# Example code that may emit warnings
x = 5
if x == 5:
    warnings.warn("x is equal to 5!")

# Catch warnings as exceptions
try:
    # Example code that may emit warnings
    x = 5
    if x == 5:
        warnings.warn("x is equal to 5!")
except Warning as w:
    print("Caught warning as exception:", w)
```

In this example, we first define our custom `warn_to_exception` function that accepts the same arguments as the `showwarning` function. This function raises an exception of the same type as the warning category (i.e., `DeprecationWarning`, `PendingDeprecationWarning`, etc.) with the given message, filename, and line number.

Next, we set the `warnings.showwarning` function to our custom `warn_to_exception` function by calling `warnings.showwarning = warn_to_exception`.

In the code that may emit warnings, we test the value of `x` and emit a warning using `warnings.warn("x is equal to 5!")` if `x` is equal to 5.

Finally, we wrap the code that may emit warnings in a `try`-`except` block that catches any warnings as exceptions and handles them appropriately. In this example, we simply print the warning message, but in a real application, we might take more meaningful action.
