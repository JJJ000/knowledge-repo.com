---
title: Constructing a single instance in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A singleton in Python can be created by using the `\_\_new\_\_` method of the class.
---

**Contents**

[TOC]

### Definition
A singleton is a class that allows only a single instance of itself to be created, and usually gives simple access to that instance.

### Creating a Singleton in Python

To create a singleton in Python, we can use the `__new__` method. This method is called when an instance of a class is created, and it allows us to control the creation of the instance. By overriding this method, we can ensure that only one instance of the class is ever created.

### Example

Here is an example of a singleton in Python:

```python
class Singleton:
    _instance = None
    def __new__(cls):
        if not cls._instance:
            cls._instance = super().__new__(cls)
        return cls._instance
```

This class ensures that only one instance of the `Singleton` class can ever be created. To use it, we simply need to call the `__new__` method:

```python
s = Singleton()
```

### Advantages

Using singletons in Python can be useful in a variety of situations. For example, they can be used to ensure that only one instance of a database connection is ever created, or to control access to a shared resource. They also provide a simple way to access a single instance of a class.
