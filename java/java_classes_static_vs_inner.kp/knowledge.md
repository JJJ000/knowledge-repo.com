---
title: Comparing static classes and inner classes in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A static class is a class that is declared with the static keyword, while an inner class is a class defined within another class.
---

**Contents**

[TOC]

### Static Class
A static class is a class that cannot be instantiated and is used to store static members. It is declared by using the static keyword before the class name. A static class can contain only static members such as constants, methods, and variables. It cannot contain instance variables and methods.

### Inner Class
An inner class is a class that is defined inside another class. It has access to all of the members of its outer class, including private members. An inner class can be declared either static or non-static. A non-static inner class has an implicit reference to its containing class and can access both static and instance members of the containing class. A static inner class does not have an implicit reference to its containing class and can only access static members of the containing class.
