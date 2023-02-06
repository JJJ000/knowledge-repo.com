---
title: String objects cannot be changed once they have been created
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In Java, an immutable String is an object whose state cannot be modified once it has been created.
---

**Contents**

[TOC]

# Definition

In Java, an immutable object is an object whose state cannot be changed after it is created. This means that any fields in the object can not be changed, and any methods that modify the state of the object will not have any effect.

# Benefits

Immutability has a number of benefits in Java. One of the most important benefits is that it makes it easier to write thread-safe code. When two threads are accessing an immutable object, there is no need to worry about the object being modified by one thread while the other thread is trying to access it. This also makes it easier to reason about the code, since it is much simpler to understand a system that is not changing its state.

# Examples

Java provides several built-in immutable classes, such as String, Integer, and BigInteger. These classes all have methods that return new objects instead of modifying the existing object. For example, the String class provides a concat() method that returns a new String object instead of modifying the existing one.

# Drawbacks

Although immutability has many benefits, it can also be a source of performance issues. Since immutable objects cannot be modified, any changes to them require creating a new object. This can be expensive in terms of both memory and CPU time. As a result, it is important to be aware of this trade-off when designing an application.
