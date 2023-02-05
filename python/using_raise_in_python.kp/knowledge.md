---
title: What is the syntax for using the "raise" keyword in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The raise keyword is used to manually raise an exception in Python.
---

**Contents**

[TOC]

## Syntax

The syntax for the `raise` keyword in Python is as follows:

```
raise [Exception [, args [, traceback]]]
```

## Explanation

The `raise` keyword is used to raise an exception. It is used to throw an exception when a specific condition occurs. The `Exception` argument can be either an instance or class of an exception. The `args` argument is optional and can be used to provide additional information about the exception. The `traceback` argument is also optional and can be used to provide a traceback object for the exception.

## Example

Here is an example of how to use the `raise` keyword in Python:

```
try:
    # some code
except Exception:
    # handle exception
    raise Exception("My custom exception message")
```

In this example, we are raising an exception with a custom message if an exception occurs in the `try` block.
