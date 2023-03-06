---
title: The class does not have any member objects
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Classes in Python have class-level attributes and instance-level attributes, so the class itself does not have an objects member.
---

**Contents**

[TOC]

Section 1: Introduction
Python is an object-oriented programming language, which means that everything in Python is considered as an object. Objects are instances of a class and are created using constructors. It is through these objects that we interact with the data and methods of the underlying class. However, there are cases where we might need to refer to a class without creating any objects of that class. In this case, we are referring to a class member or a class variable. In this article, we will discuss the absence of an objects member in Python.

Section 2: Class Members
In Python, classes have two types of members, instance members, and class members. Instance members are those that belong to a specific object of a class, whereas class members are those that belong to the class itself. Class members can be accessed using the class name, and they are shared among all objects of a class. Examples of class members include class variables, class methods, and static methods. 

Section 3: No Objects Member 
Although objects are instances of a class, there is no objects member associated with a class in Python. This is because all the methods and attributes of a class are accessed through objects, and there is no need to have an objects member. It is through the objects that we can create, modify or delete instance variables. Similarly, class methods and attributes can be accessed through the class name. Hence there is no need for an objects member in Python.

Section 4: Conclusion
In conclusion, there is no objects member in Python since everything in Python is considered as an object, and we can access the methods and attributes of a class using the objects instead of directly referring to them. Class members are accessed using the class name and they are shared globally across all instances of a class. Understanding the concept of class members and their access is essential in object-oriented programming in Python.
