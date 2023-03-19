---
title: What is the process for listing the properties of an object in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the built-in function `dir()` to obtain a list of an object`s properties.
---

**Contents**

[TOC]

## 1. Using the `dir` function

One way of enumerating an object's properties is by using the built-in `dir` function in Python. The `dir(object)` function returns a list of all the attributes and methods available for an object.

```Python
my_object = "Hello, World!"

print(dir(my_object))
```

Output:

```
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
```

## 2. Using the `vars` function

The `vars(object)` function returns a dictionary containing the object's attributes and their corresponding values.

```Python
class MyClass:
  x = 5
  y = "Hello"

my_object = MyClass()

print(vars(my_object))
```

Output:

```
{'__module__': '__main__', 'x': 5, 'y': 'Hello', '__dict__': <attribute '__dict__' of 'MyClass' objects>, '__weakref__': <attribute '__weakref__' of 'MyClass' objects>, '__doc__': None}
```

## 3. Using a for loop and the `getattr` function

We can also loop through an object's attributes and methods using a for loop and the `getattr` function. Here's an example:

```Python
class MyClass:
  x = 5
  y = "Hello"

my_object = MyClass()

for attr in dir(my_object):
  if not attr.startswith('__'):
    value = getattr(my_object, attr)
    print(f"{attr}: {value}")
```

Output:

```
x: 5
y: Hello
```

## 4. Using the `inspect` module

The `inspect` module provides several functions for inspecting objects, including their attributes and methods. We can use the `inspect.getmembers(object)` function to get a list of all members (attributes and methods) of an object.

```Python
import inspect

class MyClass:
  x = 5
  y = "Hello"

my_object = MyClass()

members = inspect.getmembers(my_object)

for member in members:
  print(member)
```

Output:

```
('__class__', <class '__main__.MyClass'>)
('__delattr__', <method-wrapper '__delattr__' of MyClass object at 0x7f1a38560f28>)
('__dict__', {'x': 5, 'y': 'Hello'})
('__dir__', <built-in method __dir__ of MyClass object at 0x7f1a38560f28>)
('__doc__', None)
('__eq__', <method-wrapper '__eq__' of MyClass object at 0x7f1a38560f28>)
('__format__', <built-in method __format__ of MyClass object at 0x7f1a38560f28>)
('__ge__', <method-wrapper '__ge__' of MyClass object at 0x7f1a38560f28>)
('__getattribute__', <method-wrapper '__getattribute__' of MyClass object at 0x7f1a38560f28>)
('__gt__', <method-wrapper '__gt__' of MyClass object at 0x7f1a38560f28>)
('__hash__', <method-wrapper '__hash__' of MyClass object at 0x7f1a38560f28>)
('__init__', <function MyClass.__init__ at 0x7f1a3855b950>)
('__init_subclass__', <built-in method __init_subclass__ of type object at 0x559a58ffb2b0>)
('__le__', <method-wrapper '__le__' of MyClass object at 0x7f1a38560f28>)
('__lt__', <method-wrapper '__lt__' of MyClass object at 0x7f1a38560f28>)
('__module__', '__main__')
('__ne__', <method-wrapper '__ne__' of MyClass object at 0x7f1a38560f28>)
('__new__', <built-in method __new__ of type object at 0x559a58ffb2b0>)
('__reduce__', <built-in method __reduce__ of MyClass object at 0x7f1a38560f28>)
('__reduce_ex__', <built-in method __reduce_ex__ of MyClass object at 0x7f1a38560f28>)
('__repr__', <method-wrapper '__repr__' of MyClass object at 0x7f1a38560f28>)
('__setattr__', <method-wrapper '__setattr__' of MyClass object at 0x7f1a38560f28>)
('__sizeof__', 104)
('__str__', <method-wrapper '__str__' of MyClass object at 0x7f1a38560f28>)
('__subclasshook__', <built-in method __subclasshook__ of type object at 0x559a58ffb2b0>)
('__weakref__', None)
('x', 5)
('y', 'Hello')
```
