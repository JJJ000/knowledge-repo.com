---
title: What are the steps to create an object that cannot be changed in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Make all attributes of the object read-only and ensure that no methods or functions can modify their values after initialization.
---

**Contents**

[TOC]

## What is an Immutable Object in Python?

An immutable object in Python is an object whose state cannot be modified after it has been created. It means once the object is created, it cannot be changed anymore.

## Benefits of Immutable Objects

There are several benefits of using immutable objects in Python:

- Immutable objects are safer to use in multi-threaded code as there can be no race condition caused by object modification.
- Immutable objects are hashable which means they can be used as keys in dictionaries or elements in sets, whereas mutable objects cannot be used as keys or elements.
- Immutable objects are often more memory-efficient since they do not require additional memory for changing their state.

## How to Create an Immutable Object in Python?

Python has several built-in classes which are immutable, such as `int`, `float`, `bool`, `str`, `tuple`, and `frozenset`. However, if you need to create a custom immutable object, you can use the following techniques:

### Method 1: Using NamedTuple

`NamedTuple` is a factory function for creating tuple subclasses with named fields. You can use `NamedTuple` to create immutable objects as follows:

```python
from typing import NamedTuple

class Person(NamedTuple):
    name: str
    age: int
```

In the above code, we created a `Person` class using `NamedTuple`. Once an object of `Person` is created, its state cannot be changed.

### Method 2: Using Frozen Classes

You can also create immutable objects using frozen classes by defining the `__setattr__` method to raise an AttributeError when it is called. This prevents any attribute from being modified after the initialization of the object. 

```python
class ImmutableClass:
    __slots__ = ['a', 'b']
    def __init__(self, a, b):
        self.a = a
        self.b = b
    def __setattr__(self, attr, value):
        raise AttributeError("can't set attribute")
```

In the above code, we created a frozen class `ImmutableClass` where the `__setattr__` method has been defined. Once an object of `ImmutableClass` is created, its state cannot be changed.

## Conclusion

Immutable objects are an essential part of Python programming. With the techniques listed above, you can create your custom immutable objects and provide more safety and security to your code.
