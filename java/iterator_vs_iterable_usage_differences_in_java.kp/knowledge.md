---
title: What is the distinction between an iterator and an iterable, and how can they be utilized?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: An Iterable is an object that can be iterated over with an Iterator, and in Java, Iterables can be used with the for-each loop.
---

**Contents**

[TOC]

# Iterator
An iterator is an object that allows a programmer to traverse through all the elements of a collection, regardless of its specific implementation. It is a Java interface that provides methods to iterate over any Collection.

# Iterable
An iterable is an object that can be iterated over. It is a Java interface that provides a single method, iterator(), which returns an iterator over the object's elements.

# Difference
The main difference between an iterator and an iterable is that an iterator has methods that allow the programmer to access and modify the underlying data structure of the collection, whereas an iterable only provides a way to access the elements of the collection.

# Usage
To use an iterator in Java, you must first obtain an instance of the iterator from the collection. This can be done by calling the iterator() method on the collection. Once you have an iterator, you can use its methods to traverse the collection. To use an iterable in Java, you can simply call the for-each loop on the iterable. This will automatically create an iterator for you and allow you to traverse the collection.
