---
title: What are the distinctions between getfields and getdeclaredfields when using Java reflection?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: getFields returns the public fields of a class, while getDeclaredFields returns all fields, public, private, and protected.
---

**Contents**

[TOC]

## getFields
The `getFields()` method of the `Class` class returns an array of `Field` objects reflecting all the accessible public fields of the class or interface represented by the given `Class` object. The elements in the array returned are sorted in the order of their declaration.

## getDeclaredFields
The `getDeclaredFields()` method of the `Class` class returns an array of `Field` objects reflecting all the fields declared by the class or interface represented by the given `Class` object, including public, protected, default (package) access, and private fields, but excludes inherited fields. The elements in the array returned are not sorted and are not in any particular order.

## Difference
The main difference between `getFields()` and `getDeclaredFields()` is that `getFields()` returns only the public fields while `getDeclaredFields()` returns all the fields declared by the class, including public, protected, default (package) access, and private fields, but excludes inherited fields.
