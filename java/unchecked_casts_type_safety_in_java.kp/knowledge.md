---
title: Verifying the correctness of a type when casting without any checks
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: An unchecked cast in Java is an explicit type conversion that does not check if the conversion is valid at runtime.
---

**Contents**

[TOC]

### Definition
An unchecked cast is a typecast in Java that does not check the validity of the cast at compile time. It is used when a programmer wants to bypass the type checking done by the compiler.

### Syntax
The syntax for an unchecked cast is as follows: 

`(ClassName) objectName`

### Examples
A common example of an unchecked cast is when casting an `Object` to a `String`: 

`String str = (String) obj;`

### Impact
Unchecked casts can lead to runtime errors if the cast is invalid. It is generally recommended to avoid unchecked casts whenever possible and instead use type-safe methods such as the `instanceof` operator or the `Class.isInstance()` method.
