---
title: How to iterate through the hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To loop through a HashMap in Java, use the for-each loop to iterate over the entrySet of the HashMap.
---

**Contents**

[TOC]

### Preparation

Before attempting to loop through a HashMap in Java, there are a few steps that need to be taken.

1. Create a HashMap object.
2. Add key-value pairs to the HashMap.

### Using the EntrySet

The most common way to loop through a HashMap in Java is to use the `entrySet()` method. This method returns a `Set` object containing all of the entries in the HashMap. 

1. Create an `Iterator` object to loop through the `Set` returned by `entrySet()`.
2. Use the `hasNext()` and `next()` methods of the `Iterator` to loop through the `Set`.
3. Use the `getKey()` and `getValue()` methods of the `Map.Entry` object to access the key and value of each entry.

### Using the KeySet

Another way to loop through a HashMap in Java is to use the `keySet()` method. This method returns a `Set` object containing all of the keys in the HashMap. 

1. Create an `Iterator` object to loop through the `Set` returned by `keySet()`.
2. Use the `hasNext()` and `next()` methods of the `Iterator` to loop through the `Set`.
3. Use the `get()` method of the HashMap to access the value associated with each key.

### Using the Values

A third way to loop through a HashMap in Java is to use the `values()` method. This method returns a `Collection` object containing all of the values in the HashMap. 

1. Create an `Iterator` object to loop through the `Collection` returned by `values()`.
2. Use the `hasNext()` and `next()` methods of the `Iterator` to loop through the `Collection`.
