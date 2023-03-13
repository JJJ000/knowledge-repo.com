---
title: The default value in python's constructor
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: A constructor in Python is a special method used to initialize objects and can have default parameter values assigned to its parameters.
---

**Contents**

[TOC]

Section 1: What is a Python constructor?
A constructor in Python is a special type of method that is used to initialize the instance variables of a class when an object is created. It lets you define what happens when an object of a class is created. The constructor method is automatically called when an object is created.

Section 2: How do you create a constructor in Python?
To create a constructor in Python, you need to define a method with the special name __init__(). This method takes the self parameter which refers to the object being created, and any other parameters that you want to define.

Example:

class MyClass:
    def __init__(self, arg1, arg2):
        self.first_variable = arg1
        self.second_variable = arg2

In this example, __init__() is the constructor method for the MyClass class. It takes two arguments arg1 and arg2, and initializes the instance variables first_variable and second_variable respectively.

Section 3: What are default values in a constructor?
Default values are values that are assigned to parameters in a function or constructor, which are used in case the function or constructor is called without providing a value for those parameters. Default values are useful when you want to ensure that the function or constructor works even if it is called without all its parameters.

Example:

class MyClass:
    def __init__(self, arg1=10, arg2=20):
        self.first_variable = arg1
        self.second_variable = arg2

In this example, the constructor for MyClass takes two arguments arg1 and arg2, both of which have default values of 10 and 20 respectively. If an object of MyClass is created without specifying any arguments, the constructor will use these default values.

Section 4: Conclusion
A constructor in Python is a special method that is used to initialize the instance variables of a class when an object is created. To create a constructor, you need to define a method with the special name __init__(). Default values are values that are assigned to the parameters of a function or constructor, which are used if the function or constructor is called without providing a value for those parameters.
