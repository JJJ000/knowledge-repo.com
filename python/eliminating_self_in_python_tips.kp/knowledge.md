---
title: What are some ways to prevent using 'self' explicitly in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use class methods or instance methods instead of defining standalone functions.
---

**Contents**

[TOC]

## Introduction

Python is a perfect object-oriented programming language that was designed in such a way that it allows developers to define their classes and objects. However, the use of explicit `self` can be overwhelming at times, and developers often wonder how they can reduce its use. In this article, we'll discuss some best practices that can help you avoid explicit `self` in Python.

## Use Class Methods

Class methods are methods that are bound to the class and not the instance of the class. Class methods receive the class itself as the first parameter, which is `cls` by convention, and not the instance of the class. Therefore, you can use class methods to avoid the use of explicit `self`.

```python
class MyClass:
    @classmethod
    def my_class_method(cls, arg1, arg2):
        # do something
```

In the above example, we define a class method called `my_class_method`. The first parameter is `cls`, which represents the class itself. Therefore, we can use `cls` instead of `self` for class-level operations.

## Use Static Methods

Static methods are similar to class methods, except that they do not receive the class as the first parameter. Therefore, they can be used to avoid the use of explicit `self` or `cls`.

```python
class MyClass:
    @staticmethod
    def my_static_method(arg1, arg2):
        # do something
```

In the above example, we define a static method called `my_static_method`. As there is no implicit reference to `self` or `cls`, you can use static methods to perform operations that do not depend on the state of the object or class.

## Use Inner Functions

You can define inner functions within a class method or instance method. You can then call them without using explicit `self` or `cls`.

```python
class MyClass:
    def __init__(self):
        self.my_var = 123

    def my_method(self, arg1, arg2):
        def my_inner_func():
            # access self.my_var without explicit self
            return self.my_var

        # do something
        return my_inner_func()
```

In the above example, we define an inner function called `my_inner_func`, which is defined within `my_method`. You can call `my_inner_func` to access `self.my_var`, as it's a closure in the scope of `my_method`.

## Use Data Classes

Finally, if you're working with Python 3.7 or newer, you can use data classes. Data classes define a class with default attributes that you can initialize using plain `__init__` method. You can put the data handling code in the data class itself.

```python
from dataclasses import dataclass

@dataclass
class MyClass:
    my_var: int

    def my_method(self):
        # access self.my_var without explicit self
        return self.my_var
```

In the above example, we define a data class called `MyClass`. The `my_var` variable is defined in the class. You can access the value of `my_var` without explicit `self` within `my_method`.

## Conclusion

There are several ways to avoid the use of explicit `self` in Python. You can use class methods and static methods when there's no need to access the individual object's variables. Also, you can define inner functions to put the data handling code in the function body itself. If you're using Python 3.7 or newer, you can use data classes defined to work with Python objects that purely carry data. The above tips can help you write clear and concise code that is easy to read and maintain.
