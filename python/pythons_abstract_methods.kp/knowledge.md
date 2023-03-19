---
title: Python's methods that are not implemented and have no body are referred to as abstract methods
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Abstract methods are methods that are declared but do not have any implementation in the abstract base class and must be overridden in the subclass.
---

**Contents**

[TOC]

What are Abstract methods:

Abstract methods in Python are methods that are declared but do not have a definition inside the class. These methods are meant to be implemented by the child classes that inherit from the parent class. The parent class is known as the abstract class and cannot be instantiated. The child classes must provide an implementation of the abstract methods in order to be considered valid.


Defining Abstract Methods:

To define an abstract method in Python, we use the `abc` module which stands for Abstract Base Classes. This module provides a decorator `@abstractmethod` that we can use to decorate methods that are meant to be abstract. For example:

```python
from abc import ABC, abstractmethod

class MyAbstractClass(ABC):
    @abstractmethod
    def my_abstract_method(self):
        pass
```

This code defines an abstract class `MyAbstractClass` that has an abstract method `my_abstract_method`. The `@abstractmethod` decorator marks the method as abstract and ensures that child classes must provide an implementation for it.


Using Abstract Methods:

To use an abstract method, we must first create a child class that inherits from the abstract class and provides an implementation for the abstract method. For example:

```python
class MyChildClass(MyAbstractClass):
    def my_abstract_method(self):
        print("Hello World!")
```

This code defines a child class `MyChildClass` that provides an implementation for the `my_abstract_method`. Now we can create an object of the `MyChildClass` and call the `my_abstract_method` on it.

```python
my_object = MyChildClass()
my_object.my_abstract_method()
```

Output:

```
Hello World!
```

This code creates an object of `MyChildClass` and calls the `my_abstract_method` on it which prints "Hello World!".


Summary:

Abstract methods in Python are methods that are declared but not defined in the abstract class. Child classes that inherit from this abstract class must provide an implementation for these methods. Abstract methods are defined using the `@abstractmethod` decorator from the `abc` module. Child classes also inherit the abstract methods from the parent class. In order for a class to be considered valid, it must provide an implementation for all of the abstract methods.
