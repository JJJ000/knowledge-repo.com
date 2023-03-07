---
title: What is the process of comparing the type of an object in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can compare the type of an object in Python using the isinstance() function.
---

**Contents**

[TOC]

# Introduction

In Python, we can determine the type of an object using the built-in `type()` function. However, sometimes we need to compare the type of an object with another type. In this tutorial, we will explore various ways to compare the type of an object in Python.

## Using the `isinstance()` Function

The `isinstance()` function is used to check if an object is an instance of a class or a subclass. We can use the `isinstance()` function to compare the type of an object with a specified type. Here's an example:

```python
a = 5
if isinstance(a, int):
    print('a is an integer')
```

This code will print `a is an integer` because we are checking if the object `a` is an instance of the `int` class.

## Using the `type()` Function

We can also compare the type of an object using the `type()` function. The `type()` function returns the type of the object. Here's an example:

```python
a = 'hello'
if type(a) == str:
    print('a is a string')
```

This code will print `a is a string` because we are checking if the type of the object `a` is equal to the `str` type.

## Using the `__class__` Attribute

Every object in Python has a `__class__` attribute that returns the type of the object. We can compare the type of an object using the `__class__` attribute. Here's an example:

```python
class Person:
    pass

p = Person()
if p.__class__ == Person:
    print('p is an instance of Person')
```

This code will print `p is an instance of Person` because we are checking if the type of the object `p` is equal to the `Person` type.

## Using the `type()` Function with `issubclass()` Function

We can also compare the type of an object using the `type()` function along with the `issubclass()` function. The `issubclass()` function is used to check if a class is a subclass of another class. Here's an example:

```python
class Animal:
    pass

class Dog(Animal):
    pass

d = Dog()
if issubclass(type(d), Animal):
    print('d is a type of Animal')
```

This code will print `d is a type of Animal` because we are checking if the type of the object `d` is a subclass of `Animal`.
