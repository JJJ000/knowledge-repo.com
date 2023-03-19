---
title: Comprehending the dissimilarity between __getattr__ and __getattribute__
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The difference between \_\_getattr\_\_ and \_\_getattribute\_\_ in Python is that \_\_getattr\_\_ is called only when an attribute is not found in the usual places, while \_\_getattribute\_\_ is called every time an attribute is accessed.
---

**Contents**

[TOC]

## Introduction
`__getattr__` and `__getattribute__` are two of the special methods in Python that allow classes to define custom behavior for attribute access on instances. At first glance, they may seem interchangeable, but there are important differences in their behavior that distinguish them from each other. In this article, we will explore these differences and how they impact the way we use these methods in practice.

## Overview
`__getattr__` and `__getattribute__` are both methods that can override the default behavior of attribute access in Python. The main difference is their timing and scope of operation. 

`__getattr__` is only called when an attribute is not found via normal attribute lookup. It is called as a last resort, after all other attribute resolution methods have failed. This means that `__getattr__` is used for getting attributes that are not defined on an object.

`__getattribute__` is called for every attribute access, whether the attribute exists or not. It is called before any other method of attribute lookup, including `__getattr__`. This means that `__getattribute__` is used for controlling how attribute access is performed, even when the attribute exists.


## Examples

### `__setattr__`

```python
class Example:
    def __init__(self, value):
        self._value = value
    def __getattr__(self, name):
        print(f"__getattr__ called for {name}")
        return "foo"
    
ex = Example(42)

print(ex._value)    # 42 - `_value` is defined and accessible normally
print(ex._foo)    # "foo" - `_foo` is not defined so __getattr__ is called
```

In this example, `__getattr__` is used for getting attributes that are not defined on an object. When we attempt to access the `_foo` attribute on the `ex` instance of `Example`, `__getattr__` is called since `_foo` does not exist. In contrast, when we access the `_value` attribute, it is defined and accessible normally.

### `__getattribute__`

```python
class Example:
    def __init__(self, value):
        self._value = value
    def __getattribute__(self, name):
        print(f"__getattribute__ called for {name}")
        if name.startswith("_"):
            # Accessing a private attribute - raise AttributeError
            raise AttributeError(f"'Example' object has no attribute '{name}'")
        else:
            # Accessing a public attribute - return it normally
            return object.__getattribute__(self, name)
        
ex = Example(42)

print(ex.__dict__)    # Error - __getattribute__ raises AttributeError for private attribute access
```

In this example, `__getattribute__` is used for controlling how attribute access is performed, even when the attribute exists. When we attempt to access the `__dict__` attribute on the `ex` instance of `Example`, `__getattribute__` is called since every attribute access is routed through it. In this case, since `__dict__` starts with an `_`, it is considered private and `__getattribute__` raises an `AttributeError` instead of returning its value.

## Conclusion
In conclusion, `__getattr__` and `__getattribute__` are two special methods in Python that allow classes to define custom behavior for attribute access on instances. While they may seem interchangeable, they have important differences in their behavior that can impact their usage. `__getattr__` is used for getting attributes that are not defined on an object, while `__getattribute__` is used for controlling how attribute access is performed, even when the attribute exists. Understanding these differences can be crucial in creating robust, maintainable Python code.
