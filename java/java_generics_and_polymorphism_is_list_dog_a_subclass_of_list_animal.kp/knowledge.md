---
title: Is list<dog> a child of list<animal>? why doesn't Java generics exhibit implicit polymorphism?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, List<Dog> is not a subclass of List<Animal>, because Java generics are not implicitly polymorphic.
---

**Contents**

[TOC]

### No
List<Dog> is not a subclass of List<Animal>.

### Why Java Generics are Not Implicitly Polymorphic
1. Generics are implemented using type erasure, which means that at runtime all generic type information is removed. This means that the compiler doesn't have enough information at runtime to determine the type of the object.

2. Generics are not covariant, which means that a type parameter cannot be substituted with a subtype. For example, List<Dog> is not a subtype of List<Animal> because it is not guaranteed that all objects in the List<Dog> are also of type Animal.

3. Generics are not reified, which means that they are not represented as actual classes at runtime. This means that the compiler cannot determine the actual type of the generic type at runtime.
