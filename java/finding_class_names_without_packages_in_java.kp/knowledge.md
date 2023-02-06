---
title: What is the name of a class without the package?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the Class.getSimpleName() method.
---

**Contents**

[TOC]

1. Using `Class.getSimpleName()`
   
   The `Class.getSimpleName()` method can be used to get the name of a class without the package name.
   
2. Using `Class.getName()`
   
   The `Class.getName()` method can be used to get the fully qualified name of a class including the package name. We can then use `String.substring()` to extract the class name without the package name.

3. Using `Class.getCanonicalName()`

   The `Class.getCanonicalName()` method can be used to get the fully qualified name of a class including the package name. We can then use `String.substring()` to extract the class name without the package name.

4. Using `Class.toString()`

   The `Class.toString()` method can be used to get the fully qualified name of a class including the package name. We can then use `String.substring()` to extract the class name without the package name.
