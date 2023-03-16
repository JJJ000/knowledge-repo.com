---
title: Is it advisable to implement name mangling in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Yes, name mangling can be used in Python to avoid name clashes in class attributes.
---

**Contents**

[TOC]

Introduction

Name mangling is a technique used in many programming languages, including Python. Its purpose is to make it harder for developers to accidentally overwrite attributes or methods in a subclass. In Python, name mangling is achieved by adding two underscores before a variable or method name. 

In this article, we will discuss the pros and cons of using name mangling in Python.

Section 1: Pros of using name mangling 

1.1) Preventing accidental overriding 

One of the main advantages of using name mangling is that it helps prevent accidental overriding of attributes or methods in subclasses. If a subclass has a method or attribute with the same name as a parent class, name mangling ensures that the subclass's version of the attribute or method is used instead of the parent class's version.

1.2) Encapsulation 

Name mangling also helps with encapsulation. By making attributes and methods private, developers can limit the scope of these elements, making them inaccessible to code outside the current class. Name mangling takes this one step further by making it harder for developers to accidentally access or modify private attributes and methods.

Section 2: Cons of using name mangling 

2.1) Less readable code 

One of the disadvantages of using name mangling is that it can make code less readable. As a programmer, it can be difficult to remember which attributes or methods have been mangled and which have not. This can make it harder for others to read and understand your code, leading to more bugs and mistakes.

2.2) False sense of security 

Another disadvantage of using name mangling is that it can give developers a false sense of security. Name mangling does not provide complete encapsulation, as it is still possible to access mangled attributes and methods if you know the mangled name. If someone really wants to access or modify a private element, they will find a way to do so, regardless of whether or not it has been mangled.

Section 3: Conclusion 

In conclusion, whether or not to use name mangling in Python depends on the specific project and the preferences of the developer or development team. If you place a high value on encapsulation and want to protect your attributes and methods from accidental modification or overriding, name mangling may be a good choice. However, if you prioritize readability and simplicity, it may be better to avoid name mangling altogether. Whatever you decide, it's important to remember that name mangling is not a silver bullet - it should be used in conjunction with other programming practices to provide a more comprehensive level of security and encapsulation.
