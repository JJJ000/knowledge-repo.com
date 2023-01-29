---
title: Determine the type of class at runtime
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The generic type of a class can be determined at runtime using the Class.getGenericSuperclass() method.
---

**Contents**

[TOC]

### Using Reflection
Reflection is a powerful tool available in Java that allows us to inspect classes, interfaces, fields and methods at runtime, without knowing the names of the classes, methods etc. at compile time.

Using this tool, we can get the generic type of a class at runtime. To do this, we first get the Class object of the class we are interested in. Then, we call the getGenericSuperclass() method on the Class object. This returns the generic superclass of the class, which is the generic type of the class.

### Using Type Erasure
Type erasure is a process by which generic type information is removed from a class or method at compile time. This means that the generic type information is not available at runtime.

However, it is possible to get the generic type of a class at runtime using type erasure. This can be done by using the getClass() method on an instance of the class to get the Class object, and then using the getGenericSuperclass() method to get the generic type of the class.
