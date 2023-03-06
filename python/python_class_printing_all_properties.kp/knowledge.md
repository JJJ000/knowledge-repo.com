---
title: Output all attributes of a Python class
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To print all properties of a Python class, use the `dir()` function which returns a list of all the attributes and methods of the given class.
---

**Contents**

[TOC]

## Section 1: Introduction

In Python, you can print all properties of a class using the built-in function `dir()`. This function returns a sorted list of all attributes and methods of any object (including classes). However, `dir()` also returns a lot of system-defined attributes that aren't relevant for most use cases. In this guide, we'll show you how to filter the `dir()` output to only include properties that are specific to your class.

## Section 2: Example usage

Consider the following example class definition:

```python
class MyClass:
    class_variable = 42
    
    def __init__(self, x, y):
        self.x = x
        self.y = y
        
    def foo(self):
        return self.x + self.y
    
    def bar(self, z):
        return self.foo() * z
```

To print all properties of this class, you can simply call the `dir()` function on an instance of the class:

```python
my_instance = MyClass(1, 2)
print(dir(my_instance))
```

This will output a lot of information, including system-defined attributes like `__class__` and `__hash__`. To filter out these attributes and only show properties that are specific to `MyClass`, you can use a list comprehension to check for the `__class__` attribute:

```python
my_instance = MyClass(1, 2)
print([attr for attr in dir(my_instance) if not attr.startswith('__')])
```

This will output `['bar', 'foo', 'x', 'y']`, which are the names of all methods and instance variables in `MyClass`.

## Section 3: Conclusion

Using the `dir()` function along with list comprehensions, you can easily print all properties of a Python class. By filtering out system-defined attributes, you can focus specifically on the attributes and methods that are unique to your class.
