---
title: Can you explain the function of "mro()"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: mro() returns a list of the method resolution order for a class.
---

**Contents**

[TOC]

# Introduction

The `mro()` function in Python is used to return the method resolution order (MRO) of a class. It is a powerful tool that helps in determining the order in which methods are searched for and called during method resolution.

# Syntax

The syntax of `mro()` function is as follows:

```
class_name.mro()
```

Here, `class_name` is the name of the class whose MRO is to be determined.

# Working

The `mro()` function works by returning a list of class objects that are involved in the method resolution of a particular class. This list is in the order in which the methods are searched for during the method resolution.

The MRO is calculated using a depth-first algorithm that takes into account the inheritance hierarchy of the class. The algorithm first looks for the method in the current class, then in its parent class, then in the grandparent class, and so on until it reaches the root object. If a method is not found at any level, it returns an error.

# Return Value

The `mro()` function returns a list of class objects in the order in which the methods are searched for during the method resolution.

For example:

```python
class A:
    def foo(self):
        print("A.foo()")
        
class B:
    pass

class C(A, B):
    pass

print(C.mro())
```

The `mro()` function will return `[<class '__main__.C'>, <class '__main__.A'>, <class '__main__.B'>, <class 'object'>]`. This indicates that when we call the `foo()` method on an instance of class `C`, Python will first search for the method in class `C`, then in class `A`, then in class `B`, and finally in the base `object` class.
