---
title: A class in Python that is implemented as "private."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: In Python, a private class is one that uses a naming convention to indicate that it should not be accessed outside of its own module.
---

**Contents**

[TOC]

# Introduction

In Python, it is not possible to create "private" classes, in the sense that access to a class or its attributes can be restricted to only within the class. However, there are some conventions and techniques that can be used to achieve similar functionality.

# Naming convention

A common convention used in Python is to prefix attributes and methods that should be considered as "private" with an underscore (_). This does not actually prevent access from outside the class, but it indicates to other developers that these members are not intended to be used outside the class.

```python
class MyClass:
    def __init__(self):
        self.public_attribute = "I am public"
        self._private_attribute = "I am private"
    
    def public_method(self):
        print("This is a public method")
    
    def _private_method(self):
        print("This is a private method")
```

# Name mangling

Python also supports a form of "name mangling" by prefixing member names with two underscores (__) leading to a name-mangled form of the attribute name. This can be useful to prevent accidental access to members that are considered private.

```python
class MyClass:
    def __init__(self):
        self.public_attribute = "I am public"
        self.__private_attribute = "I am private"
    
    def public_method(self):
        print("This is a public method")
    
    def __private_method(self):
        print("This is a private method")
    
    def call_private_method(self):
        self.__private_method()
```

# Encapsulation

The private class functionality can be emulated by making use of encapsulation. Encapsulation is the technique of hiding the internal workings of an object from the outside world, and only exposing a public interface by which the object can be interacted with. This can be achieved by defining only the public methods of the class, and using them to manipulate the private attributes of the class.

```python
class MyClass:
    def __init__(self):
        self.__private_attribute = "I am private"
    
    def public_method(self):
        print("This is a public method")
        self.__private_method()
    
    def __private_method(self):
        print("This is a private method")
```

# Conclusion

Although Python does not have a strict "private" class functionality, by using naming conventions, name mangling, and encapsulation, it is possible to achieve similar functionality. However, it is important to remember that these are conventions and not actual access control mechanisms.
