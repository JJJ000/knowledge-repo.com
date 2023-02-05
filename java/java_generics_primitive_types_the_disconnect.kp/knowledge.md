---
title: What is the reason that Java generics do not support primitive types?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Java Generics are implemented using Object types, so primitive types are not supported.
---

**Contents**

[TOC]

##### Primitive Types
Primitives are not objects, they are values that are directly stored in the memory. Primitive types are not classes and therefore can not be used as type parameters. 

##### Type Erasure
In Java, generic type information is only available during compile time, and is removed during runtime. This process is known as type erasure. This means that any type information that is set during compile time is erased during runtime, leaving the generic class with no knowledge of the type parameter. 

##### Performance
Using primitive types instead of their wrapper classes can lead to improved performance. However, because of type erasure, this cannot be done when using generics.
