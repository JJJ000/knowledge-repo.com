---
title: What is the process for executing code when a class becomes a subclass?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Override the `\_\_init\_subclass\_\_()` method in the parent class.
---

**Contents**

[TOC]

## Introduction
In Python, a class can be subclassed using inheritance. Sometimes, we might want to perform certain operations or execute some code when a class is subclassed. In this article, we will learn how to run code when a class is subclassed in Python.


## Using the __init_subclass__ method
Python provides a special method called `__init_subclass__` which can be used to define actions that will be executed automatically when a class is subclassed. Here's an example:

```python
class MyParentClass:
    def __init_subclass__(cls):
        print("Subclassing", cls)

class MyChildClass(MyParentClass):
    pass
```

When we execute the above code, we get the following output:

```
Subclassing <class '__main__.MyChildClass'>
```

Here, we defined a parent class called `MyParentClass` which contains the `__init_subclass__` method. This method will be executed automatically when a class is subclassed from `MyParentClass`. In the example, we are simply printing a message to the console when a subclass is created.


## Passing arguments to __init_subclass__
Sometimes, we might want to pass arguments to the `__init_subclass__` method. Here's an example:

```python
class MyParentClass:
    def __init_subclass__(cls, my_arg):
        print("Subclassing with arg:", my_arg)

class MyChildClass(MyParentClass, my_arg="Hello"):
    pass
```

When we execute the above code, we get the following output:

```
Subclassing with arg: Hello
```

In this example, we are passing an argument called `my_arg` to the `__init_subclass__` method. We are using keyword arguments to specify the arguments that should be passed to the method.


## Using metaclasses
Python also provides an advanced feature called metaclasses that can be used to customize class creation. Here's an example:

```python
class MyMetaClass(type):
    def __new__(cls, name, bases, attrs):
        print("Creating class:", name)
        return super().__new__(cls, name, bases, attrs)

class MyParentClass(metaclass=MyMetaClass):
    pass

class MyChildClass(MyParentClass):
    pass
```

When we execute the above code, we get the following output:

```
Creating class: MyParentClass
Creating class: MyChildClass
```

In this example, we defined a metaclass called `MyMetaClass` which contains the `__new__` method. This method is called whenever a new class is defined. We are using the `super()` function to call the `__new__` method of the parent class. We are also printing a message to the console when a class is created.

We then defined a parent class called `MyParentClass` and specified its metaclass as `MyMetaClass`. We also defined a child class called `MyChildClass` which subclasses from `MyParentClass`. When we create the `MyChildClass` class, both the parent and child class are created, and the `__new__` method of the metaclass is called twice.
