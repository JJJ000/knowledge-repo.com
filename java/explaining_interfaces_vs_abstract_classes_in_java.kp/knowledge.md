---
title: What is the best way to explain the distinction between an interface and an abstract class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: An Interface defines a set of methods that must be implemented, while an Abstract class may provide some implementation and define methods that must be overridden.
---

**Contents**

[TOC]

### Definition
An interface in Java is a collection of abstract methods and constants that form a common set of base rules/guidelines for any class that implements it. An abstract class is a special type of class that cannot be instantiated and is used as a base class for other classes.

### Similarities
Both interfaces and abstract classes allow developers to define the basic structure of a class without having to provide all of the details. They also both provide a way to create a contract between a class and its subclasses.

### Differences
The primary difference between an interface and an abstract class is that an interface can only contain abstract methods and constants, while an abstract class can contain both abstract methods and concrete methods. Additionally, an interface can be implemented by any number of classes, while an abstract class can only be extended by a single class. Finally, an interface can contain static methods, while an abstract class cannot.
