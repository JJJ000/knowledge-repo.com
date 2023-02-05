---
title: Examine two Java objects that may contain null values
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Two objects in Java can be compared using the `equals()` method, which returns a boolean value depending on whether or not the two objects are equal, accounting for possible null values.
---

**Contents**

[TOC]

## Comparing Equality
In Java, two objects can be compared for equality using the `equals()` method.  This method returns a boolean value indicating whether or not the two objects are equal. The `equals()` method should be overridden for custom objects, as the default implementation of `equals()` only checks for reference equality.

When comparing two objects with possible null values, the `equals()` method should first check for null values before attempting to compare the two objects. This can be done by using the `==` operator to check for null values. If either of the objects is null, the `equals()` method should return false.

## Comparing Identity
In addition to comparing two objects for equality, it is also possible to compare them for identity. This can be done using the `==` operator, which checks for reference equality. If the two objects have the same reference, the `==` operator will return true.

When comparing two objects with possible null values, the `==` operator should first check for null values before attempting to compare the two objects. This can be done by using the `==` operator to check for null values. If either of the objects is null, the `==` operator should return false.
