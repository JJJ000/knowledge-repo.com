---
title: What is the way to determine the quantity of arguments in a Python function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can find the number of arguments of a Python function using the `func.\_\_code\_\_.co\_argcount` attribute.
---

**Contents**

[TOC]

## Using the inspect module
Python provides the `inspect` module which can be used to retrieve information about objects such as classes and functions. This module includes the `getargspec` function which returns information about the arguments of a function.

```python
import inspect

def func(arg1, arg2, *args, **kwargs):
    pass

print(len(inspect.getargspec(func).args))
```

This will output `2`, which is the number of regular arguments `arg1` and `arg2`.


## Using the signature method
In Python 3, the `inspect` module includes a new `Signature` object which provides more detailed information about function signatures. We can use this object to count the number of arguments.

```python
import inspect

def func(arg1, arg2, *args, **kwargs):
    pass

sig = inspect.signature(func)
print(len(sig.parameters))
```

This will also output `2`.

## Using the function's __code__ object
The function object in Python includes a `__code__` attribute which provides information about the function's compiled bytecode. The `__code__` object includes an attribute `co_argcount` which provides the number of arguments.

```python
def func(arg1, arg2, *args, **kwargs):
    pass

print(func.__code__.co_argcount)
```

This will also output `2`.

## Conclusion
These are three different ways you can determine the number of arguments of a Python function. The first two methods use the `inspect` module to retrieve information about the function signature, while the last method uses the function's `__code__` attribute.
