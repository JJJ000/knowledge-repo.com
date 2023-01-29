---
title: Transform set into list without generating a new list
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: It is not possible to convert a Set to a List without creating a new List in Java.
---

**Contents**

[TOC]

### Option 1: Using `Set.toArray()`

The `Set.toArray()` method can be used to convert a `Set` to a `List` without creating a new `List`. This method returns an array containing all the elements of the `Set`. The array can then be passed to the `Arrays.asList()` method to create a `List` from the `Set`.

### Option 2: Using `Collections.list()`

The `Collections.list()` method can also be used to convert a `Set` to a `List` without creating a new `List`. This method takes a `Set` as a parameter and returns a `List` containing all the elements of the `Set`.

### Option 3: Using `Stream API`

The `Stream API` can also be used to convert a `Set` to a `List` without creating a new `List`. This can be done by using the `Set.stream()` method to get a `Stream` from the `Set` and then using the `Stream.collect()` method to collect the elements of the `Stream` into a `List`.

### Option 4: Using `Iterator`

The `Iterator` can also be used to convert a `Set` to a `List` without creating a new `List`. This can be done by using the `Set.iterator()` method to get an `Iterator` from the `Set` and then looping over the `Iterator` to add the elements to a `List`.
