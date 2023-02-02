---
title: I only passed one argument to the method, but I received an error saying that it was expecting two positional arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The argument being passed is likely a tuple, which counts as one argument.
---

**Contents**

[TOC]

# Overview
This error occurs when a function is called with too many arguments. In Python, a function can only take as many arguments as it is declared to take.

# Causes
This error occurs when a function is called with more arguments than it is declared to take. This can happen when the function is called with incorrect arguments, when a function is called with too many arguments, or when a function is called with an incorrect number of arguments.

# Examples
For example, if a function is declared to take one argument and is called with two arguments, this error will occur:

```
def method(arg1):
    # do something

method(arg1, arg2)

TypeError: method() takes 1 positional argument but 2 were given
```

# Solutions
To solve this error, make sure that the function is being called with the correct number of arguments. If the function is being called with the correct number of arguments, check that the arguments are the correct type and that they are in the correct order.
