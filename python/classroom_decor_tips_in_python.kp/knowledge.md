---
title: What are ways to adorn a classroom?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the @decorator\_name syntax to add additional functionality to an existing function or class in Python.
---

**Contents**

[TOC]

Section 1: Understanding Class Decoration

Before learning how to decorate a class in Python, it is important to understand class decoration itself. In Python, class decoration refers to modifying or adding functionality to a class using a decorator. A decorator in Python is a function that takes another function or class as an input and returns a new function or class. The decorator function can modify the existing class or function behavior by adding new properties or methods or by modifying existing ones.

Section 2: Decorator Function to Decorate a Class

To decorate a class in Python, you can define a decorator function that takes the class as an argument, modifies it, and returns the modified class. Here is an example of a decorator function that adds a new method to a class:

``` python
def add_method(cls):
    def new_method(self, x):
        return x * 2
    cls.new_method = new_method
    return cls
```

This decorator adds a new method `new_method` to the `cls` (class) by defining a new method `new_method` inside the decorator and then assigning it to the `cls` using the `cls.new_method=new_method` statement.

Section 3: Applying the Decorator to a Class

To apply the decorator to a class, you simply need to use the `@` symbol followed by the decorator function name, just before the class definition. Here's an example:

``` python
@add_method
class MyClass:
    def __init__(self, val):
        self.val = val
    def calculate(self):
        return self.val * 2
```

In this example, the `add_method` decorator is applied to the `MyClass` class using the `@add_method` syntax. The resulting class will have the `new_method` added to it as a new method, in addition to the existing `__init__` and `calculate` methods.

Section 4: Decorator Classes to Decorate a Class

In addition to using a decorator function, you can also use a decorator class to decorate a class in Python. Here's an example:

``` python
class AddMethod:
    def __init__(self, cls):
        self.cls = cls
    def __call__(self):
        def new_method(self, x):
            return x * 2
        self.cls.new_method = new_method
        return self.cls

@AddMethod
class MyClass:
    def __init__(self, val):
        self.val = val
    def calculate(self):
        return self.val * 2
```

In this example, the `AddMethod` decorator class takes the `cls` (class) as an input in the `__init__` method and modifies the existing class by adding a new method `new_method` inside the `__call__` method. The `__call__` method returns the modified class. The `@AddMethod` syntax is used to apply this decorator to the `MyClass` class.
