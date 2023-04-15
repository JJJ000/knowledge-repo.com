---
title: What criteria does the arraylist's contains() method use to determine if an object is present?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The contains() method of an ArrayList in Java evaluates objects by comparing them to the elements already stored in the list using the equals() method.
---

**Contents**

[TOC]

### Overview
The `contains()` method is a part of the `ArrayList` class in Java, and is used to determine if a particular object is present in the `ArrayList`. This method is used to check if an object is present in the `ArrayList`, and returns a boolean value indicating the presence of the object.

### Syntax
The syntax for the `contains()` method is as follows:

`ArrayList.contains(Object o)`

### Parameters
The `contains()` method takes a single parameter of type `Object`, which is the object to be checked for presence in the `ArrayList`.

### Return Value
The `contains()` method returns a boolean value indicating the presence of the object in the `ArrayList`. If the object is present in the `ArrayList`, the method returns `true`, else it returns `false`.
