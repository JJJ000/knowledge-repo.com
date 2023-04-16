---
title: What is the syntax for obtaining the name of a function as a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the built-in function `str` to get a function name as a string in Python.
---

**Contents**

[TOC]

# Section 1: Using the inspect Module
The inspect module in Python provides several useful functions to help get information about live objects such as modules, classes, methods, functions, etc. One of the functions, `inspect.getframeinfo()`, can be used to get the name of a function as a string.

# Section 2: Example Usage

Below is an example of how to use the `inspect.getframeinfo()` function to get the name of a function as a string:

```python
import inspect

def example_function():
    frame = inspect.getframeinfo(inspect.currentframe())
    print(frame.function)

example_function()
```

The above code will print out the string `example_function`.

# Section 3: Additional Information

The `inspect.getframeinfo()` function can also be used to get the filename, line number, and other information about the function. For more information, please see the [Python Documentation](https://docs.python.org/3/library/inspect.html#inspect.getframeinfo).

# Section 4: Alternative Methods

Another way to get the name of a function as a string is to use the `func_name` attribute of a function object. For example:

```python
def example_function():
    pass

print(example_function.func_name)
```

The above code will print out the string `example_function`.
