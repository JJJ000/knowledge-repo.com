---
title: What is the method of passing data used in Java: "pass-by-reference" or "pass-by-value"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Java uses `pass-by-value` for primitive types, and `pass-by-reference` for objects.
---

**Contents**

[TOC]

### Pass-by-Value
In Java, primitive types (e.g. int, char, boolean) are passed by value. This means that when a primitive type is passed as an argument to a method, a copy of the value is made and passed to the method. The original value remains unchanged, even if the value of the argument is changed within the method.

### Pass-by-Reference
In Java, objects are passed by reference. This means that when an object is passed as an argument to a method, a reference to the object is passed, rather than a copy of the object. Any changes made to the object within the method will be reflected in the original object.
