---
title: How do == and equals() differ in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The == operator checks if two values are equal in terms of reference, while the equals() method checks if two values are equal in terms of content.
---

**Contents**

[TOC]

### Syntax

The `==` operator is a comparison operator, while the `equals()` method is a method of the Object class. 

### Comparison

The `==` operator compares two objects to see if they are the same object in memory. The `equals()` method compares two objects to see if they are logically equivalent.

### Overriding

The `equals()` method can be overridden in a subclass to provide an appropriate implementation of object equality. The `==` operator cannot be overridden.

### Usage

The `==` operator should be used to compare primitive values, while the `equals()` method should be used to compare objects.
