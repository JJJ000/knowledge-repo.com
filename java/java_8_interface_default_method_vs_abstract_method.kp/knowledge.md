---
title: What is the difference between using a default method in a Java 8+ interface and an abstract method?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use an interface default method when you want to provide a default implementation for all implementing classes, and an abstract method when you want to require all implementing classes to provide their own implementation.
---

**Contents**

[TOC]

### Abstract Method
Abstract methods are methods that do not have an implementation and must be implemented by the subclass. They are declared using the abstract keyword and can only be used in an abstract class. Abstract methods are used when you want to define the structure of a class, but not its implementation.

### Default Method
Default methods are methods that have an implementation and can be used in an interface. They are declared using the default keyword and can be used in both interfaces and abstract classes. Default methods are used when you want to provide an implementation for a method in an interface, but also allow for the implementation to be overridden by a subclass.
