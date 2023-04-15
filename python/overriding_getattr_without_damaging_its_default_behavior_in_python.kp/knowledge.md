---
title: What is the correct approach to modify the default behavior of __getattr__ without causing any disruptions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use `super().\_\_getattr\_\_` to access the default behavior of the parent class.
---

**Contents**

[TOC]

## Introduction
Python provides a special method called `__getattr__()` to handle attribute access that is not explicitly defined in a class. This method can be overridden to define custom behavior for attribute access. However, if we override `__getattr__()` without taking care of the default behavior, it may cause unexpected errors and behavior in the program.

In this tutorial, we will explore how to properly override `__getattr__()` without breaking the default behavior in Python.

## Understanding __getattr__()
First, let's understand how `__getattr__()` works in Python. When Python encounters an attribute access operation that is not explicitly defined in a class, it calls the `__getattr__()` method of the class to handle the request. Here's the basic syntax of `__getattr__()`:

```
class MyClass:
    def __getattr__(self, name):
        # handle the attribute access
```

The `__getattr__()` method takes two arguments:
- `self`: the instance of the class on which the attribute access operation was performed
- `name`: the name of the attribute that was accessed

The method should return the value of the requested attribute. If the attribute is not found, the method should raise an `AttributeError`.

## Overriding __getattr__() without breaking default behavior
To override `__getattr__()` without breaking the default behavior, we can follow these steps:

### 1. Use super() to call the default __getattr__() implementation
When we override a special method like `__getattr__()`, we should use `super()` to call the implementation of the method in the parent class. This allows us to preserve the default behavior of the method. Here's an example:

```
class MyClass:
    def __getattr__(self, name):
        # custom behavior
        return super().__getattr__(name)
```

In this example, we define our custom behavior for attribute access, but then we call `super().__getattr__(name)` to invoke the default implementation and get the value of the attribute.

### 2. Check if the attribute exists in __dict__
Another way to avoid breaking the default behavior is to check if the attribute exists in the instance's `__dict__` attribute. This is the dictionary that stores the instance's attributes. If the attribute is found, we can return its value. If not, we can call `super().__getattr__(name)` to handle the request. Here's an example:

```
class MyClass:
    def __getattr__(self, name):
        if name in self.__dict__:
            return self.__dict__[name]
        else:
            return super().__getattr__(name)
```

### 3. Raise AttributeError for unknown attributes
If none of the above conditions are met, that means the attribute access operation is for an unknown attribute. In this case, we should raise an `AttributeError` to indicate that the attribute does not exist. Here's the updated code:

```
class MyClass:
    def __getattr__(self, name):
        if name in self.__dict__:
            return self.__dict__[name]
        else:
            raise AttributeError(f"'{self.__class__.__name__}' object has no attribute '{name}'")
```

In this code, we check if the attribute exists in the instance's `__dict__` attribute. If it does, we return its value. Otherwise, we raise an `AttributeError` with a message that states the name of the unknown attribute.

### 4. Handling AttributeError exceptions
If we want to handle `AttributeError` exceptions raised by `__getattr__()`, we can use a try-except block around the attribute access operation. Here's an example:

```
try:
    value = obj.unknown_attribute
except AttributeError:
    # handle the error
```

In this code, we try to access the unknown attribute using the `obj.unknown_attribute` syntax. If an `AttributeError` is raised, we handle the exception in the `except` block.

## Conclusion
In this tutorial, we learned how to override `__getattr__()` without breaking the default behavior in Python. We saw that we can use `super()` to call the default implementation of the method, check if the attribute exists in the instance's `__dict__` attribute, and raise `AttributeError` for unknown attributes. We also saw how to handle `AttributeError` exceptions in our code.
