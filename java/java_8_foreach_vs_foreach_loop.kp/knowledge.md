---
title: Comparison of Java 8 iterable.foreach() and foreach loop
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Iterable.forEach() is a built-in Java 8 method that allows for a more concise and functional approach to looping through a collection, while a traditional foreach loop is a more verbose approach.
---

**Contents**

[TOC]

### Iterable.forEach()
Iterable.forEach() is an inbuilt method in Java 8 that allows for an action to be performed on each element of a collection. It takes a single argument, a Consumer object which is an interface that defines an action to be taken on an object. This action is performed for each element of the collection. It is a void method and does not return anything.

### foreach loop
A foreach loop is a type of loop that is used to iterate over a collection or array. It takes two arguments, the first being the element in the collection or array and the second is the action to be performed on that element. The foreach loop is a syntactic sugar for the Iterable.forEach() method and is essentially a shortcut for the same.

### Advantages of Iterable.forEach()
- It is a concise and readable way to iterate over a collection
- It is a void method and does not return anything
- It can be used with Lambda expressions to perform more complex operations

### Advantages of foreach loop
- It is a concise and readable way to iterate over a collection
- It is a type of loop and can be used to iterate over a collection or array
- It is a syntactic sugar for the Iterable.forEach() method and is essentially a shortcut for the same.
