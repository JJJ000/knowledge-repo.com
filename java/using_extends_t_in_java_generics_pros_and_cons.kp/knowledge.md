---
title: What are the circumstances for using <? extends t> instead of <t> in Java generics and what are the potential drawbacks of making this switch?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Java generics require <? extends T> instead of <T> when the generic type is used as a parameter type for a method, and using <? extends T> instead of <T> can cause compile-time errors if the method requires the generic type to be a superclass of the declared type.
---

**Contents**

[TOC]

**When to Use <? extends T>**

When using generics, <? extends T> should be used when you want to allow for a generic type to be a subclass of a certain type. This is useful when you have a method that needs to accept any subclass of a certain type but not the type itself.

**When to Use <T>**

<T> should be used when you want to allow for a generic type to be of a certain type. This is useful when you have a method that needs to accept a certain type, or any of its subclasses.

**Downside of Switching**

The downside of switching between <? extends T> and <T> is that it can lead to confusion. If you use <T> when you should have used <? extends T>, then you may end up with a method that accepts a type that you don't want it to accept. This can lead to bugs and unexpected behavior.
