---
title: How does instanceof differ from class.isassignablefrom(...)?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: instanceof checks if an object is an instance of a particular class, whereas Class.isAssignableFrom(...) checks if a class is a subclass of another class.
---

**Contents**

[TOC]

### Instanceof

The instanceof operator is used to check if the object is an instance of a particular class. It returns true if the object is an instance of the specified class, otherwise it returns false.

### Class.isAssignableFrom(...)

Class.isAssignableFrom(...) checks if a class is a subtype of another class. It returns true if the specified class is the same as, or is a superclass or superinterface of, the class or interface represented by the specified object. Otherwise it returns false.
