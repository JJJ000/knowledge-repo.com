---
title: The error message indicating that the name 'self' has not been defined
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The error occurs when the keyword `self` is used outside of a class definition.
---

**Contents**

[TOC]

# Introduction

The `NameError: name 'self' is not defined` error occurs when the keyword `self` is referenced outside the scope of a class method or attribute. This error is common in object-oriented programming, especially in Python.

In this article, we will discuss the reasons for this error and how to fix it.

# Using `self` inside a class

The keyword `self` is used in Python to refer to the instance of a class. It is used inside class methods and attributes to access and modify the instance's properties.

For example:

```python
class MyClass:
    def __init__(self, name):
        self.name = name

    def say_hello(self):
        print(f"Hello, my name is {self.name}.")
```

In this example, we define a class `MyClass` with two methods. The `__init__` method initializes a new instance of the class with a `name` attribute. The `say_hello` method uses the `self` keyword to access the instance's `name` attribute and print a message.

# Using `self` outside a class

If you try to use the `self` keyword outside a class, you will get the `NameError: name 'self' is not defined` error.

For example:

```python
self.name = "John"
```

In this example, we are trying to set the `name` attribute of an instance, but `self` is not defined because we are outside the scope of a class method.

# Fixing the error

To fix the `NameError: name 'self' is not defined` error, make sure that you are using the `self` keyword inside a class method or attribute. If you are outside a class, remove the `self` keyword and use a variable to refer to the instance.

For example:

```python
class MyClass:
    def __init__(self, name):
        self.name = name

    def say_hello(self):
        print(f"Hello, my name is {self.name}.")

# Create an instance
my_object = MyClass("John")

# Call the method
my_object.say_hello()

# Set the attribute
my_object.name = "Mary"
```

In this example, we define a class `MyClass` with an `__init__` method to create an instance with a `name` attribute and a `say_hello` method to print a message with the instance's name. We then create an instance and call the method. Finally, we set the instance's name attribute to a new value. 

# Conclusion

The `NameError: name 'self' is not defined` error occurs when the `self` keyword is referenced outside a class method or attribute. To fix this error, make sure that you are using `self` inside a class method or attribute, and remove it when outside a class.
