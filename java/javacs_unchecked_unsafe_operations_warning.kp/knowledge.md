---
title: What is causing the javac compiler to give the warning about using unchecked or unsafe operations?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The `uses unchecked or unsafe operations` warning is issued by javac when code uses operations that may result in incorrect or unexpected behavior due to lack of type safety.
---

**Contents**

[TOC]

### Unsafe Operations
Unsafe operations are operations that are not type-safe or do not check for potential runtime errors. These operations can lead to unexpected behavior or crashes. Examples of unsafe operations include accessing array elements without bounds checking, performing arithmetic operations on primitive types without checking for overflow, and casting objects to incompatible types.

### Generics
Generics are a feature of the Java language that allow for type-safe operations. Generics allow for type parameters to be specified for classes and methods. This allows for the compiler to check for potential type mismatches at compile-time and prevent runtime errors.

### Unchecked Operations
Unchecked operations are operations that are not checked by the compiler for potential runtime errors. These operations can lead to unexpected behavior or crashes. Examples of unchecked operations include accessing array elements without bounds checking, performing arithmetic operations on primitive types without checking for overflow, and casting objects to incompatible types.

### Javac Warning
The "uses unchecked or unsafe operations" warning is issued by the javac compiler when it detects code that uses unchecked or unsafe operations. This warning is issued to alert the developer that their code may be prone to unexpected behavior or crashes.
