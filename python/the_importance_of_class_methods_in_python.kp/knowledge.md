---
title: What is the goal of having class methods?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Class methods in Python are used to define methods that are bound to the class and not the instance of the class.
---

**Contents**

[TOC]

## Overview 

Python is an object-oriented programming language that supports the concept of classes and objects. In Python, methods are functions that are defined inside the class, and they can operate on the data members of the class. There are two types of methods in Python: instance methods and class methods. In this article, we will discuss the purpose of class methods in Python.

## What are class methods?

A class method is a method that is bound to the class and not the instance of the class. This means that the method can be called on the class itself instead of an instance of the class. Class methods are defined using the @classmethod decorator. The first parameter of a class method is always the class itself, which is typically referred to as cls.

## The Purpose of Class Methods

### 1. Accessing class-level attributes

One of the primary uses of class methods is to access class-level attributes. A class-level attribute is an attribute that is shared among all the instances of the class. Since a class method is bound to the class and not the instance, it can access the class-level attributes without having an instance of the class.

### 2. Creating alternate constructors

Another use of class methods is to create alternate constructors. An alternate constructor is a class method that creates and returns an instance of the class using different parameters than the __init__ method. Since a class method can be called on the class itself, it can be used to create instances of the class without having to use the __init__ method.

### 3. Modifying class-level attributes

Class methods can also be used to modify the class-level attributes. This is useful when you want to change the value of an attribute for all instances of the class. Since a class method is bound to the class, it can access and modify the class-level attribute without having an instance of the class.

### 4. Providing an interface for subclasses

Finally, class methods can be used to provide an interface for subclasses. By defining a class method in the parent class, you can provide a template or a blueprint for the child classes. Subclasses can override the class method to provide their own implementation. This allows you to create a consistent interface across all the subclasses. 


## Conclusion 

In conclusion, class methods are a powerful feature of Python that allow you to work with class-level attributes and provide alternate constructors, modify class-level attributes, and provide an interface for subclasses. By understanding the purpose of class methods, you can write more efficient and effective Python code.
