---
title: What is the equivalent of java's static methods in kotlin?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Kotlin, static methods are replaced by top-level functions and companion object functions.
---

**Contents**

[TOC]

### Top-level Functions
In Kotlin, static methods are replaced by top-level functions. These are functions that are declared at the same level as classes, outside of any class. They can be called without having to create an instance of a class.

### Companion Objects
Kotlin also has the concept of companion objects. These are objects that are declared inside a class, but outside of any function. They can be used to hold static members.

### Object Declarations
Kotlin also has the concept of object declarations. These are singleton objects that are declared at the same level as classes. They can be used to hold static members.

### @JvmStatic Annotation
Finally, Kotlin also has the concept of the @JvmStatic annotation. This annotation can be used to mark a top-level function or a member of a companion object as a static method. This allows the function or member to be accessed from Java code as if it were a static method.
