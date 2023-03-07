---
title: What is the process for installing a default dictionary in a certain order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the OrderedDict class from the collections module to implement an ordered, default dict in Python.
---

**Contents**

[TOC]

# Introduction 
A dictionary in Python is a data structure that contains a collection of key-value pairs. The default dictionary is a subclass of the built-in dictionary in Python, and it provides a default value whenever a key error occurs. The default value can be any default factory function. 

An ordered dictionary is a dictionary where the order of the keys is maintained in each insertion. 

In this guide, we will learn how to implement an ordered, default dict in Python.

# Section 1: Using Ordered Dict and Default Dict

The Python collections module provides two classes that can be used to implement an ordered, default dictionary: OrderedDict and defaultdict.

To create an ordered, default dictionary, we can use both classes together. Here is how to implement it:

```python
from collections import OrderedDict, defaultdict

class DefaultOrderedDict(OrderedDict):
  def __init__(self, default_factory=None, *a, **kw):
    if (default_factory is not None and
        not callable(default_factory)):
      raise TypeError('first argument must be callable')
    OrderedDict.__init__(self, *a, **kw)
    self.default_factory = default_factory

  def __getitem__(self, key):
    try:
      return super().__getitem__(key)
    except KeyError:
      return self.__missing__(key)

  def __missing__(self, key):
    if self.default_factory is None:
      raise KeyError(key)
    self[key] = value = self.default_factory()
    return value

  def __reduce__(self):
    args = iter(())
    if self.default_factory is not None:
      args = iter((self.default_factory,))
    return type(self), args, None, None, iter(self.items())

d = DefaultOrderedDict(int)
```

In the above code, we define a new class called `DefaultOrderedDict`, which inherits from both `OrderedDict` and `defaultdict`. In the constructor of the class, we initialize the `default_factory` argument to the None value. If the `default_factory` is set to None, it raises a KeyError exception. 

The `__getitem__` method in the class tries to get the value of a given key using the `super()` function. If a KeyError occurs, the `__missing__` method will be called, which creates a new key and sets the default value for this key using the `default_factory` function.

# Section 2: Testing the Default Ordered Dict

Let's test the new ordered, default dictionary:

```python
d['apple'] += 1
d['banana'] += 2
d['pear'] += 3
d['apple'] += 2
```

Output:

```
DefaultOrderedDict([('apple', 3), ('banana', 2), ('pear', 3)])
```

As you can see, the `DefaultOrderedDict` class correctly stored the values in the order they were added.

# Conclusion
In this guide, we learned how to create an ordered, default dictionary in Python. We used two built-in Python classes, OrderedDict and defaultdict, to achieve this. By using these classes together, we were able to create a dictionary that maintains the order of the keys and provides a default value for missing keys.
