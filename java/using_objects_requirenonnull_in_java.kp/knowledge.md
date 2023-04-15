---
title: What are the benefits of using objects.requirenonnull()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Objects.requireNonNull() is used to ensure that an object reference passed as a parameter to a method is not null.
---

**Contents**

[TOC]

### Definition
Objects.requireNonNull() is a static method in the Java Objects class that throws a NullPointerException if the object passed to it is null.

### Benefits
1. Improved Readability: Using Objects.requireNonNull() makes the code more readable since it clearly indicates that the object is checked for null.
2. Improved Performance: Using the method can improve performance since it is a static method that is only called once instead of performing multiple checks.
3. Improved Code Quality: Using the method ensures that the code is more robust by avoiding potential NullPointerExceptions.

### Use Cases
Objects.requireNonNull() should be used when a method or constructor argument is expected to be non-null. This can be used to ensure that the code does not throw a NullPointerException and is more robust.
