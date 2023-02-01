---
title: What are the distinctions between an abstract class and an interface in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: An abstract class in Python allows for both the declaration of abstract methods (which must be implemented by any concrete subclasses) and the implementation of concrete methods, whereas an interface in Python only allows for the declaration of abstract methods.
---

**Contents**

[TOC]

# Abstract Class

An abstract class is a class that contains one or more abstract methods. Abstract methods are methods that are declared, but contain no implementation. Abstract classes cannot be instantiated, and require subclasses to provide implementations for the abstract methods.

# Interface

An interface is a class that contains only abstract methods. It is not possible to instantiate an interface, and it can only be used as a type. All methods declared in an interface must be implemented by any class that implements the interface.

# Differences

- An abstract class can contain both abstract and non-abstract methods, while an interface can only contain abstract methods.
- An abstract class can have instance variables, while an interface cannot.
- An abstract class can provide a partial implementation of a class, while an interface cannot.
- A class can extend only one abstract class, while it can implement multiple interfaces.
