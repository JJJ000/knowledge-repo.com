---
title: Retrieving characteristics of a class
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: In order to get attributes of a class in Python, you can use the dir() function or access attributes directly by using the dot notation.
---

**Contents**

[TOC]

# Overview 

In Python, you can get the attributes of a class using different methods. Typically, you need to define a class and then access its attributes through instance objects or the class itself. In this tutorial, you will learn how to get attributes of a class using the following methods:

- Using the `dir()` function
- Using the `vars()` function
- Using `inspect` module
- Using the `__dict__` attribute


# Using the `dir()` function

The `dir()` function in Python returns a list of all attributes of a module, object, or class. To get the attributes of a class, you need to pass the class name or an instance object to the `dir()` function. For example:

```python
class MyClass:
    attr1 = 'foo'
    attr2 = 123

dir(MyClass)
```

Output:
```
['__doc__', '__module__', 'attr1', 'attr2', ...]
```

As you can see, `dir(MyClass)` returns a list of attributes, including the `__doc__` and `__module__` special attributes.


# Using the `vars()` function

The `vars()` function in Python returns a dictionary of the attributes of an object or a class. To get the attributes of a class, you need to pass the class name or an instance object to the `vars()` function. For example:

```python
class MyClass:
    attr1 = 'foo'
    attr2 = 123
    
vars(MyClass)
```

Output:
```
{'__doc__': None, '__module__': '__main__', 'attr1': 'foo', 'attr2': 123}
```

As you can see, `vars(MyClass)` returns a dictionary of attributes, including the `__doc__` and `__module__` special attributes.


# Using `inspect` module

The `inspect` module in Python provides a range of functions for introspection of objects. You can use the `inspect.getmembers()` function to get the attributes of a class. For example:

```python
import inspect

class MyClass:
    attr1 = 'foo'
    attr2 = 123

members = inspect.getmembers(MyClass)
print(members)
```

Output:
```
[('__doc__', None), ('__module__', '__main__'), ('attr1', 'foo'), ('attr2', 123)]
```

As you can see, `inspect.getmembers(MyClass)` returns a list of tuples, where each tuple represents an attribute and its value, including the `__doc__` and `__module__` special attributes.


# Using the `__dict__` attribute

Every class in Python has a `__dict__` attribute that stores the class attributes as a dictionary. To get the attributes of a class, you can access its `__dict__` attribute. For example:

```python
class MyClass:
    attr1 = 'foo'
    attr2 = 123

print(MyClass.__dict__)
```

Output:
```
{'__module__': '__main__', 'attr1': 'foo', 'attr2': 123, '__dict__': <attribute '__dict__' of 'MyClass' objects>, '__weakref__': <attribute '__weakref__' of 'MyClass' objects>, '__doc__': None}
```

As you can see, `MyClass.__dict__` returns a dictionary of attributes, including the `__doc__` and `__module__` special attributes.
