---
title: What is the process for initializing the base (super) class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To initialize the base (super) class in Python, you can call the super() function with the class and subclass names as arguments, and then call the \_\_init\_\_() method of the super class.
---

**Contents**

[TOC]

# Introduction
When creating a Python class that is a subclass, it is typical to also inherit the attributes and methods of the superclass. However, before we can use the attributes and methods of the superclass, we must first initialize it.

# Using super()
The easiest way to initialize the superclass in Python is to use the `super()` function. This function returns a temporary object of the superclass, which we can use to call its methods.

Here is an example of how to use `super()` to initialize the superclass:

```python
class Superclass:
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2

class Subclass(Superclass):
    def __init__(self, arg1, arg2, arg3):
        super().__init__(arg1, arg2)
        self.arg3 = arg3
```

In the example above, we have a superclass `Superclass` with an `__init__()` method that takes two arguments `arg1` and `arg2`. We also have a subclass `Subclass` that inherits from `Superclass` and has an `__init__()` method that takes three arguments `arg1`, `arg2`, and `arg3`.

To initialize the superclass in the subclass, we use the `super().__init__()` method to call the `__init__()` method of the superclass and pass it `arg1` and `arg2`. We then assign `arg3` to an instance variable in the subclass.

# Using the superclass name
Another way to initialize the superclass in Python is to directly call the `__init__()` method of the superclass using its name. This is useful when you have multiple superclasses or when you want to call a specific method in the superclass.

Here is an example of how to initialize the superclass using its name:

```python
class Superclass:
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2

class Subclass(Superclass):
    def __init__(self, arg1, arg2, arg3):
        Superclass.__init__(self, arg1, arg2)
        self.arg3 = arg3
```

In the example above, we have the same superclass `Superclass` and subclass `Subclass`. However, instead of using `super().__init__()`, we call `Superclass.__init__()` and pass it `self`, `arg1`, and `arg2`. We then assign `arg3` to an instance variable in the subclass.

# When to use each method
Both methods have their advantages and disadvantages. Using `super()` is preferred when you are working with multiple inheritance or when you want to support cooperative inheritance. It also makes your code more flexible to changes in the superclass's implementation.

Using the superclass name is useful when you need to call a specific method in the superclass or when you have multiple superclasses with the same method names. However, this method is not as flexible and can cause issues if the superclass's implementation changes.

# Conclusion
Initializing the superclass is an important step when creating a Python class that is a subclass. It allows us to inherit the attributes and methods of the superclass and use them in our subclass. Both the `super()` function and the superclass name can be used to initialize the superclass, each with their own advantages and disadvantages.
