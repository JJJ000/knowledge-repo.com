---
title: Looping through and deleting elements from a map
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To iterate over and remove from a map in Java, use the Iterator.remove() method.
---

**Contents**

[TOC]

### Iterating Over a Map

The most common way to iterate over a map in Java is to use the `forEach()` method on the `Map` interface. This method takes a `BiConsumer` as an argument, which is a functional interface that accepts two arguments and returns no result.

The `BiConsumer` is passed two arguments: the key and the value of the map entry. The code inside the `BiConsumer` can then be used to process the key and value in any way desired.

### Removing From a Map

Removing entries from a map in Java is done using the `remove()` method on the `Map` interface. This method takes the key of the entry to be removed as an argument and returns the corresponding value.

The `remove()` method returns `null` if the key is not present in the map. This can be used to check if the key was present before attempting to remove it.

### Alternative Iteration Methods

An alternative way to iterate over a map in Java is to use the `entrySet()` method on the `Map` interface. This method returns a `Set` of `Map.Entry` objects, which represent the individual entries in the map.

The `Map.Entry` objects can then be iterated over using a `for-each` loop, and the entries can be removed from the map by calling the `remove()` method on the `Map.Entry` object.

### Conclusion

Iterating over and removing from a map in Java can be done using the `forEach()` and `remove()` methods on the `Map` interface, or using the `entrySet()` and `remove()` methods.
