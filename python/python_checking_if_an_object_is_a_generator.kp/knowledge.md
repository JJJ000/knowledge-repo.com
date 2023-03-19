---
title: What is the method for verifying if an object is a generator object in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Check if the object is an instance of the `generator` class using the `isinstance` function.
---

**Contents**

[TOC]

## Introduction
In Python, generators are special functions that allow you to generate a sequence of values one at a time. They are useful when working with large datasets or when you want to generate values on the fly. Sometimes, you may want to check if an object is a generator object in order to perform specific tasks related to it. This tutorial will walk you through the steps required to check if an object is a generator object in Python.

## Using the `inspect` Module

The easiest way to check if an object is a generator object is by using the `inspect` module. This module contains a `isgenerator()` function that you can use to check if an object is of type generator. Here is an example:

```python
import inspect

def my_generator():
    yield 1
    yield 2
    yield 3

gen_obj = my_generator()

if inspect.isgenerator(gen_obj):
    print("Object is a generator!")
else:
    print("Object is not a generator!")
```

In this example, we define a generator function `my_generator()` and create a generator object `gen_obj` from it. We then use the `isgenerator()` function to check if `gen_obj` is a generator object. If it is, we print a message saying that the object is a generator. Otherwise, we print a message saying that the object is not a generator.

## Using the `types` Module

Another way to check if an object is a generator object is by using the `types` module. This module contains the `GeneratorType` class which you can use to test if an object is of type generator. Here is an example:

```python
import types

def my_generator():
    yield 1
    yield 2
    yield 3

gen_obj = my_generator()

if isinstance(gen_obj, types.GeneratorType):
    print("Object is a generator!")
else:
    print("Object is not a generator!")
```

In this example, we define a generator function `my_generator()` and create a generator object `gen_obj` from it. We then use the `isinstance()` function to check if `gen_obj` is an instance of the `GeneratorType` class. If it is, we print a message saying that the object is a generator. Otherwise, we print a message saying that the object is not a generator.

## Using the `__name__` Attribute

The `__name__` attribute can also be used to check if an object is a generator object. When a generator function is defined, its `__name__` attribute is set to `'<generator>'`. You can check if an object is a generator object by testing if its `__name__` attribute is equal to `'<generator>'`. Here is an example:

```python
def my_generator():
    yield 1
    yield 2
    yield 3

gen_obj = my_generator()

if gen_obj.__name__ == '<generator>':
    print("Object is a generator!")
else:
    print("Object is not a generator!")
```

In this example, we define a generator function `my_generator()` and create a generator object `gen_obj` from it. We then check if `gen_obj` has its `__name__` attribute set to `'<generator>'`. If it does, we print a message saying that the object is a generator. Otherwise, we print a message saying that the object is not a generator.

## Conclusion

In this tutorial, we have seen three different ways to check if an object is a generator object in Python. You can use the `inspect` module, the `types` module, or the `__name__` attribute to perform this check. Choose the one that best suits your needs and enjoy working with generators!
