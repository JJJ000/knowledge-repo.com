---
title: What is the reason for not automatically calling superclass __init__ methods?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Superclass \_\_init\_\_ methods are not automatically invoked in Python because child classes may want to customize their initialization process without invoking the initialization process of their parent classes.
---

**Contents**

[TOC]

Section 1: Background
In Python, inheritance allows for the creation of a subclass that inherits attributes and methods from a superclass. When a subclass is created, it can override methods of its superclass by defining a new implementation for the same method name. However, the superclass's implementation can still be accessed from the subclass. 

Section 2: Superclass __init__ methods 
Superclasses usually have an `__init__` method which initializes instances of the class. If a subclass does not have an `__init__` method, Python will automatically look for and call the superclass's `__init__` method. However, if a subclass has its own `__init__` method, the superclass's `__init__` method will not be called automatically. 

Section 3: Overriding superclass __init__ method
Subclasses can override the superclass's `__init__` method, but when they do, they must call the superclass's `__init__` method explicitly to initialize the inherited attributes. This can be done using the `super()` function. For example, in the following code, `super().__init__()` is called in the `__init__` method of the `Car` class to initialize the `name` attribute inherited from `Vehicle` class:

```
class Vehicle:
    def __init__(self, name):
        self.name = name

class Car(Vehicle):
    def __init__(self, name, color):
        self.color = color
        super().__init__(name)
```

Section 4: Flexibility and control
By not automatically invoking the superclass's `__init__` method, Python provides flexibility and control. Subclasses can completely override the initialization process or partially initialize the instance using a combination of their own logic and that of the superclass. This also avoids unintended side effects from the superclass initializer in cases where a subclass may have different required parameters or might need to perform additional initialization steps.
