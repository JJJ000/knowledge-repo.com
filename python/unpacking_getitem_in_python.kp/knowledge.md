---
title: Comprehending the __getitem__ function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The \_\_getitem\_\_ method in Python is used to define the behavior for accessing an item using an index or key in an object.
---

**Contents**

[TOC]

## Overview

The `__getitem__` method in Python is a magic method that allows an instance of a class to be accessed using the square bracket notation (`[]`). It is also known as the indexing operator. The `__getitem__` method allows objects to behave like sequences, mappings, or sets, depending on how it is implemented in the class.

## Syntax

The syntax for the `__getitem__` method is as follows:

```python
def __getitem__(self, key):
    # access the value associated with the given key
    return value
```

## Implementation

To implement the `__getitem__` method, you need to define it in your class. The `__getitem__` method should take a `key` argument, which represents the index or key used to access the value in the object.

The `__getitem__` method should then use the key to return the value associated with it. If the key is not valid, you may raise an appropriate exception.

## Usage

The `__getitem__` method is commonly used in classes that act like sequences, mappings, or sets. For example, if you want to create a custom list class, you can implement the `__getitem__` method to allow indexing of the list items.

```python
class MyList:
    def __init__(self, items):
        self.items = items

    def __getitem__(self, index):
        return self.items[index]
```

In this example, the `MyList` class implements the `__getitem__` method to allow indexing of the `items` list. You can then use the square bracket notation to access elements of the list instance:

```python
my_list = MyList([1, 2, 3])
print(my_list[0])   # prints 1
print(my_list[1])   # prints 2
print(my_list[2])   # prints 3
```
