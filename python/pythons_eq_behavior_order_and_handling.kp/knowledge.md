---
title: What is the order of handling __eq__ in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: In Python, \_\_eq\_\_ is handled by first checking if the two objects have the same memory address, and if not, calling the method to compare their values.
---

**Contents**

[TOC]

## Overview of __eq__ in Python

In Python, `__eq__()` is a special method used to compare two objects for equality. This method is called when we use the `==` operator to compare two objects. If `__eq__()` is not implemented in our class, the `==` operator will compare object identity (i.e., it will return True only if both objects are the same object in memory). 

## Order of Execution for __eq__ in Python

The `__eq__()` method is executed when we use the `==` operator to compare two objects. When we write `a == b`, Python will execute the following steps:

1. If `a` and `b` are the same object (i.e., they have the same memory address), return True.
2. If `a` and `b` are not instances of the same class, return False.
3. If `a` and `b` are instances of the same class, but that class does not implement `__eq__()`, return False.
4. If `a` and `b` are instances of the same class and that class implements `__eq__()`, call `__eq__()` on `a` and pass `b` as an argument. Return the result of this method call.

## Implementing __eq__ in Python

When implementing `__eq__()` in our class, we should define what equality means for our objects. For example, if we have a class representing a point in 2D space, we might define `__eq__()` like this:

```
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __eq__(self, other):
        if isinstance(other, Point):
            return self.x == other.x and self.y == other.y
        return False
```

In this implementation, two points are considered equal if they have the same `x` and `y` coordinates. We first check whether `other` is an instance of `Point` (to avoid comparing our objects with objects of other classes), and then compare their coordinates. 

## Conclusion

In conclusion, `__eq__()` is a special method used to compare objects for equality in Python. It is executed when we use the `==` operator to compare two objects. We can implement `__eq__()` in our classes to define what equality means for our objects.
