---
title: What is the distinction between using collection.stream().foreach() and collection.foreach()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Collection.stream().forEach() processes the elements in the collection in a sequential manner, while Collection.forEach() processes the elements in the collection in an unspecified order.
---

**Contents**

[TOC]

### Collection.forEach()

Collection.forEach() is a method of the Java Collection interface which is used to iterate over the elements of a Collection. It takes a single argument which is a Consumer object. The Consumer object is responsible for performing an action on each element of the Collection.

### Collection.stream().forEach()

Collection.stream().forEach() is a method of the Java Stream interface which is used to iterate over the elements of a Collection. It takes a single argument which is a Consumer object. The Consumer object is responsible for performing an action on each element of the Stream.

### Differences

The main difference between Collection.forEach() and Collection.stream().forEach() is that Collection.forEach() is used to iterate over the elements of a Collection, while Collection.stream().forEach() is used to iterate over the elements of a Stream. Additionally, Collection.stream().forEach() can be used to perform operations on the elements of a Stream, such as filtering, mapping, and reducing, while Collection.forEach() cannot.
