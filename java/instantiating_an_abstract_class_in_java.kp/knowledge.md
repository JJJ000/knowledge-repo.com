---
title: Is it possible to create an object of an abstract class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, an abstract class cannot be instantiated in Java.
---

**Contents**

[TOC]

####Overview
Abstract classes in Java are classes that cannot be instantiated. They are used to provide a common definition of a base class that multiple derived classes can share.

####Why Abstract Classes Cannot Be Instantiated
Abstract classes cannot be instantiated because they may contain abstract methods, which are methods that are declared, but not implemented. In order to use an abstract class, a non-abstract class must be derived from it that provides implementations for the abstract methods.

####Abstract Classes vs Interfaces
Abstract classes are similar to interfaces, but they can contain fields and concrete methods. Interfaces cannot contain any method implementations, only method declarations.

####Conclusion
In summary, abstract classes in Java cannot be instantiated as they may contain abstract methods that need to be implemented by a non-abstract class. Abstract classes are similar to interfaces, but they can contain fields and concrete methods.
