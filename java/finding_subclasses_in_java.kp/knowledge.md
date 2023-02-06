---
title: What is the process for locating all subclasses of a specified class in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the Class.getSubclasses() method to find all subclasses of a given class in Java.
---

**Contents**

[TOC]

#1 Using Reflection

Reflection is a powerful feature of the Java language that allows developers to inspect classes and their properties, including their subclasses. To find all subclasses of a given class, we can use the Java Reflection API.

#2 Using Class.getDeclaredClasses()

The Class.getDeclaredClasses() method returns an array of Class objects that represent all the classes and interfaces that are declared as members of the class represented by this Class object. This array includes public, protected, default (package) access, and private classes and interfaces declared by the class, but excludes inherited classes and interfaces.

#3 Using Class.getClasses()

The Class.getClasses() method returns an array of Class objects that represent all the public classes and interfaces that are members of the class represented by this Class object. This array includes the public classes and interfaces that are members of the class and declared by the class, but excludes inherited classes and interfaces.

#4 Using ClassLoader

The ClassLoader class provides a way to find all the classes that are loaded into the JVM. By using the ClassLoader.getResources() method, we can get a list of all the classes in the classpath and then iterate through them to find the ones that are subclasses of the given class.
