---
title: What is the syntax for invoking a parent class's method from a child class in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can call a parent class`s method from a child class in Python by using the super() method.
---

**Contents**

[TOC]

#1Method Resolution Order (MRO)
The Method Resolution Order (MRO) is the order in which Python looks for methods in a class when resolving method calls. The MRO is determined by the class's inheritance hierarchy. The MRO is a list of classes that are searched in order, from the class itself, to its parent classes, and so on, until it reaches the top-most class in the hierarchy (usually object).

#2Using super()
The super() function allows us to call a method from a parent class in Python. The syntax for using super() is super(ChildClass, self).methodName(). This will call the methodName() method from the parent class of the ChildClass.

#3Using the Parent Class Name
Another way to call a parent class's method from a child class is to use the parent class's name. The syntax for this is ParentClassName.methodName(self). This will call the methodName() method from the ParentClassName.

#4Using the Class Instance
The last way to call a parent class's method from a child class is to use the class instance. The syntax for this is self.ParentClassName.methodName(). This will call the methodName() method from the ParentClassName.
