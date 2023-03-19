---
title: Comparing 'python __new__ and __init__' with 'python c API __new__ and __init__'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: \_\_new\_\_ creates and returns a new instance of a class, while \_\_init\_\_ initializes the instance and sets its initial attributes.
---

**Contents**

[TOC]

Section 1: Introduction to __new__ and __init__

In Python, when an instance of a class is created, two methods are automatically called: `__new__` and `__init__`. These two methods serve different purposes during the instance creation process.

`__new__` is a special method that creates and returns a new instance of the class. It takes the class as its first argument and returns a new instance of the class. It is responsible for creating the instance of the object and initializing its attributes. 

`__init__` is a special method that initializes the newly-created object created by `__new__`. It takes the instance of the object as its first argument and initializes its attributes. 

In this article, we'll discuss the differences between `__new__` and `__init__`, and when each method should be used in Python.

Section 2: __new__ method

The `__new__` method is called when a new instance of a class is created. It is responsible for creating and returning a new instance of the class. The `__new__` method is a static method, which means it does not take any parameters from the instance of the object.

`__new__` is typically used when you need to customize the object creation process. For example, when a class inherits from an immutable object like a tuple or a string, the `__new__` method can be used to customize the behavior of the object.

Here's an example of how to use `__new__` method:

```
class MyImmutableString(str):
    def __new__(cls, value):
        obj = str.__new__(cls, value.upper())
        obj.value = value
        return obj

s = MyImmutableString("Hello world")
print(s)  # Output: HELLO WORLD
print(s.value)  # Output: Hello world
```

In this example, we create a subclass of the `str` class and override its `__new__` method. The `__new__` method converts the input value to uppercase and initializes a new attribute called `value` with the original input.


Section 3: __init__ method

The `__init__` method is called after `__new__` method and is responsible for initializing the newly-created object's attributes. It takes the instance of the object as its first argument and does not return any value.

The `__init__` method is typically used when you need to initialize the attributes of an object. Here's an example:

```
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

dog1 = Dog("Fido", "Labrador")
print(dog1.name)  # Output: Fido
print(dog1.breed)  # Output: Labrador
```

In this example, we define a `Dog` class that has two attributes, `name` and `breed`. In the `Dog` class's `__init__` method, we initialize the `name` and `breed` attributes using the arguments passed to the constructor.

Section 4: __new__ versus __init__

In summary, the `__new__` method is responsible for creating a new instance of the class, whereas `__init__` method is responsible for initializing the attributes of the object created by the `__new__` method. `__new__` is common in immutable object classes, while `__init__` is used in most other classes. In general, it is recommended to use `__init__` for most object initialization tasks, and use `__new__` only when necessary.
