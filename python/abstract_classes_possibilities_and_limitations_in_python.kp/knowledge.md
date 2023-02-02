---
title: Can abstract classes be created?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Yes, abstract classes can be created in Python using the abc (Abstract Base Class) module.
---

**Contents**

[TOC]

Yes, it is possible to make abstract classes in Python.

# Syntax

Abstract classes are created by inheriting from the `abc` module. For example:

```python
from abc import ABC, abstractmethod

class AbstractClassExample(ABC):
    @abstractmethod
    def do_something(self):
        pass
```

# Usage

Abstract classes are used to define an interface for other classes to follow. They cannot be instantiated and any class that inherits from an abstract class must implement all of its abstract methods.

# Benefits

Abstract classes can help ensure that subclasses follow a certain interface, which can help reduce code duplication and improve code readability. They also allow developers to quickly identify which classes are meant to be abstract and which are meant to be concrete.
