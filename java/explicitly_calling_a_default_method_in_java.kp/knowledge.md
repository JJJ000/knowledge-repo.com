---
title: Explicitly invoking a default method in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A default method can be explicitly called by using the class name followed by the method name.
---

**Contents**

[TOC]

### Syntax

The syntax for explicitly calling a default method in Java is: 

`ClassName.super.methodName();`

### Example

For example, if you have a class called `Foo` that extends `Bar` and `Bar` has a default method called `getName()`, then you can call the `getName()` method from `Foo` by using the following syntax: 

`Foo.super.getName();`

### Benefits

Explicitly calling a default method in Java can be beneficial when you want to override a method from a superclass and also call the default implementation. This can be done by calling the superclass's default method directly, instead of having to create an additional method in the subclass.

### Caveats

When explicitly calling a default method, it is important to keep in mind that the method must be accessible from the subclass. If the method is not accessible, then a compilation error will occur. Additionally, if the superclass's default method is overridden in the subclass, then the subclass's implementation will be called instead.
