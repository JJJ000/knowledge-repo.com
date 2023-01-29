---
title: Modify a private static final field using Java reflection
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is possible to use the Field class` set() method to change the value of a private static final field using Java reflection.
---

**Contents**

[TOC]

### Overview

Java reflection is a powerful tool that allows us to access and modify private static final fields. This can be done by using the Field class from the java.lang.reflect package.

### Getting the Field

The first step is to get a reference to the Field object. This can be done using the getDeclaredField method of the Class class. This method takes the name of the field as an argument and returns a Field object that can be used to access the field.

### Accessing the Field

Once we have a reference to the Field object, we can use the setAccessible method to make the field accessible. This will allow us to access and modify the field.

### Modifying the Field

Finally, we can use the set method of the Field class to modify the value of the field. This method takes two arguments – the object that contains the field and the new value for the field.
