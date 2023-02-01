---
title: What is the most straightforward and graceful method of describing singletons?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, the easiest way to define a singleton in Python is to use the `singleton pattern` with a class decorated with the @singleton decorator.
---

**Contents**

[TOC]

## Definition
A singleton is a class which can have only one instance. It is typically used to implement global state or provide a global interface for a system.

## Class Definition
The following class definition can be used to define a singleton in Python:

```python
class Singleton(object):
    _instance = None
    def __new__(cls):
        if not cls._instance:
            cls._instance = super(Singleton, cls).__new__(cls)
        return cls._instance
```

## Usage
The singleton can be used as follows:

```python
s = Singleton()
s.some_property = "value"
s2 = Singleton()
print s2.some_property # prints "value"
```

## Benefits
The main benefit of using a singleton is that it allows for global state to be easily managed and accessed. It also provides a global interface for a system, which makes it easier to access shared resources and services.
