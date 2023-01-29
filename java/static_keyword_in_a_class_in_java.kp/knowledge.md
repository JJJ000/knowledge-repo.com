---
title: What is the purpose of the 'static' keyword when used in a class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `static` keyword in a class in Java allows methods and variables to be accessed without creating an instance of the class.
---

**Contents**

[TOC]

### Definition
The 'static' keyword in a class in Java indicates that the particular member belongs to the class, rather than to any particular instance of that class.

### Benefits
1. Static methods can be called directly from a class, without the need to create an instance of the class.
2. Static variables are shared among all instances of a class, which can be useful for keeping track of global values.
3. Static members can be accessed without the need for a reference to an object.
4. Static methods can access static variables without the need for an instance reference.
