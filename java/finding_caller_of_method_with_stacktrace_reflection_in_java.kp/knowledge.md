---
title: What is the best way to identify the origin of a method call using stacktrace or reflection?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using reflection, you can get the calling method`s name from the StackTraceElement object obtained from the Throwable object.
---

**Contents**

[TOC]

### Using Stacktrace

1. The `Thread` class provides a `getStackTrace()` method which returns an array of `StackTraceElement` objects. 
2. Each element in the array represents a single stack frame. 
3. The `StackTraceElement` class has a `getClassName()` and `getMethodName()` methods which can be used to determine the caller of the method. 

### Using Reflection

1. The `Class` class provides a `getDeclaredMethods()` method which returns an array of `Method` objects. 
2. Each `Method` object has a `getDeclaringClass()` method which can be used to determine the class which declared the method. 
3. The `Class` class also provides a `getEnclosingMethod()` method which can be used to determine the method which invoked the method.
