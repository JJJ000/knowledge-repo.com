---
title: What is the equivalent of the c# 'var' keyword in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, the equivalent of the C# `var` keyword is the keyword `var` followed by the type of the variable.
---

**Contents**

[TOC]

##### `Object`

In Java, the equivalent of the C# 'var' keyword is the `Object` class. The `Object` class is the root of the Java class hierarchy and is a superclass of all other Java classes. It is used to declare variables that can refer to an object of any type.

##### `Object` vs `Class`

It is important to note that `Object` is not the same as a `Class` in Java. A `Class` is a template that is used to create objects, while an `Object` is an instance of a `Class`.

##### `Object` Usage

Using the `Object` keyword, a variable can be declared and initialized to refer to an object of any type. For example:

```java
Object myObject = new Object();
```

This statement creates an instance of the `Object` class and assigns it to the variable `myObject`. The variable `myObject` can now be used to refer to the object.
