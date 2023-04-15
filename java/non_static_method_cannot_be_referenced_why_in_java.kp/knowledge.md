---
title: Why is it not possible to call a non-static method from a static context?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Non-static methods must be called from an instance of the containing class, whereas static methods can be called directly from the containing class.
---

**Contents**

[TOC]

### Understanding Static and Non-Static
Static methods and variables are associated with the class, rather than any particular instance of the class. This means that static methods and variables can be accessed without creating an instance of the class.

Non-static methods and variables are associated with a particular instance of the class. To access a non-static method or variable, an instance of the class must first be created.

### Static Context
A static context is any place in the Java program where a static method or variable can be accessed. This includes the main method, static initializers, and static methods.

### Non-Static Context
A non-static context is any place in the Java program where a non-static method or variable can be accessed. This includes instance methods, constructors, and instance variables.

### Reasoning
The reason behind the error "non-static method cannot be referenced from a static context" is because it is not possible to access a non-static method or variable from a static context. The compiler will throw an error because it does not know which instance of the class to use to access the non-static method or variable.
