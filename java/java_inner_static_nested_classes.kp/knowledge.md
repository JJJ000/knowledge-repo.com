---
title: What are inner classes and static nested classes in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: An inner class is a non-static nested class, while a static nested class is a nested class that is declared static.
---

**Contents**

[TOC]

### Inner Class
An inner class is a class that is defined within another class. Inner classes are used to logically group classes that are only used in one place, increase encapsulation, and create more readable and maintainable code.

Inner classes can access all of the members (fields, methods, and nested classes) of the enclosing class, even if they have the same access modifiers.

### Static Nested Class
A static nested class is a static class that is defined within another class. Unlike an inner class, a static nested class cannot access the instance variables and methods of the enclosing class.

Static nested classes are useful when you only need to use the nested class in one place and don't need access to the instance variables or methods of the enclosing class. They are also useful for organizing related classes and improving code readability.
