---
title: Retrieving an item from a set
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Set`s iterator to retrieve an element from the Set.
---

**Contents**

[TOC]

### Using the `contains()` Method

The `contains()` method can be used to check if a Set contains a particular element. This method takes in a single argument, the element to be checked, and returns a boolean value indicating whether the element is present in the Set or not.

### Using the `iterator()` Method

The `iterator()` method can be used to iterate over the elements of a Set. This method returns an Iterator object which can be used to traverse the elements of the Set. The Iterator object provides methods like `hasNext()` and `next()` which can be used to check if the Set contains a particular element and to get the element respectively.

### Using the `forEach()` Method

The `forEach()` method can be used to iterate over the elements of a Set. This method takes in a single argument, a lambda expression, which is used to process each element of the Set. The lambda expression takes in a single argument, the element to be processed, and can be used to check if the Set contains a particular element.

### Using the `toArray()` Method

The `toArray()` method can be used to convert a Set into an array of objects. This method takes in a single argument, an array of objects, and returns an array containing the elements of the Set. The array can then be used to check if the Set contains a particular element.
