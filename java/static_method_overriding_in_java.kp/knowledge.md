---
title: What is the reason that Java does not permit the overriding of static methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Static methods are associated with a class, not an instance of a class, so they cannot be overridden since they cannot be associated with a specific instance.
---

**Contents**

[TOC]

### Reason 
Static methods are associated with a class rather than an object, and so cannot be overridden in the same way as instance methods. 

### How It Works
When a static method is invoked, the compiler determines the class to which it applies, and then binds the method call to the corresponding code. This is known as static binding. In contrast, when an instance method is invoked, the compiler determines the type of the object, and then binds the method call to the corresponding code. This is known as dynamic binding. 

### Benefits
The primary benefit of static methods is that they can be invoked without having to create an instance of the class. This can be useful for utility methods, such as methods that perform calculations or that provide data. Additionally, static methods can be used to enforce encapsulation, as they can be used to limit access to certain methods or data. 

### Disadvantages
The primary disadvantage of static methods is that they cannot be overridden. This can be a problem when a subclass needs to modify the behavior of a static method. Additionally, static methods can lead to tight coupling between classes, as they can be used to access data or methods from other classes.
