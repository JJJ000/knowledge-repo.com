---
title: What is the procedure for returning a value from the __init__ constructor in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You don`t return a value from \_\_init\_\_ in Python, as it is intended to initialize an instance of a class and doesn`t return anything.
---

**Contents**

[TOC]

## Introduction

`__init__()` is a special method in python that is invoked automatically when an object is created. This method is used to initialize the attributes of the object. However, sometimes there might be a need to return a value from `__init__()` method.

In this article, we will discuss how to return a value from `__init__()` in Python.

## Using a Return Statement

One way to return a value from `__init__()` is to use a return statement inside the method. However, it is important to note that when a class is instantiated and `__init__()` is called, the return value will be the newly created object and not the return value of the `__init__()` method.

```python
class MyClass:
    def __init__(self):
        self.value = 10
        return  # Return statement at the end

obj = MyClass()
print(obj.value)  # Output: 10
```

## Using a Factory Function

Another way to return a value from `__init__()` is by using a factory function. We can create a separate function that creates an object of the class and returns it after initializing its attributes.

```python
class MyClass:
    def __init__(self, value):
        self.value = value

def create_object(value):
    obj = MyClass(value)
    return obj

obj = create_object(10)
print(obj.value)  # Output: 10
```

## Using Static Methods

We can also use static methods to return a value from `__init__()` method. A static method is a method that belongs to the class and not to an instance of the class. This method can be called on the class itself and not on an instance of the class.

```python
class MyClass:
    def __init__(self, value):
        self.value = value

    @staticmethod
    def create_object(value):
        obj = MyClass(value)
        return obj

obj = MyClass.create_object(10)
print(obj.value)  # Output: 10
```

## Conclusion

In this article, we discussed three ways to return a value from `__init__()` method in python. We can use a return statement inside the method, a factory function, or static methods to return a value.
