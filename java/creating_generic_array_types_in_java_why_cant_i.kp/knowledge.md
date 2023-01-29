---
title: Why can't I create generic array types in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Java does not support generic array types due to type erasure.
---

**Contents**

[TOC]

### Type Erasure

In Java, generic type information is only available at compile time. Once a program is compiled, all generic type information is erased and replaced with the base type. This process is called type erasure. This means that when a program is run, there is no way to determine the type of a generic object. As a result, it is not possible to create generic array types in Java.

### Array Store Exceptions

Another reason why generic array types cannot be created in Java is due to the Array Store Exception. This exception is thrown when an attempt is made to store an object of a type other than the type of the array into the array. Since generic types are erased at compile time, it is impossible to guarantee that the objects stored in a generic array are of the correct type. As a result, the Array Store Exception is thrown when an attempt is made to create a generic array type.

### Type Safety

Lastly, generic array types cannot be created in Java due to type safety. Java requires that all objects stored in an array are of the same type. This is to ensure that the array is type-safe and that no unexpected behavior occurs. Since generic types are erased at compile time, it is not possible to guarantee that all objects stored in a generic array are of the same type. As a result, it is not possible to create generic array types in Java.
