---
title: An exception caused by attempting to create a map using collectors.tomap with null values for some of the entries
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Collectors.toMap will throw a NullPointerException if any of the entry values are null.
---

**Contents**

[TOC]

### Introduction
Collectors.toMap is a method in the Java Stream API that can be used to collect elements from a Stream into a Map. It takes two parameters, a key mapper and a value mapper, and returns a Collector that accumulates elements into a Map. However, when using Collectors.toMap with null entry values, it may throw a NullPointerException.

### What is a NullPointerException?
A NullPointerException is an exception that is thrown when a program attempts to use an object reference that has the null value. This can occur when a program tries to access a member of an object that has not been initialized, or when a program tries to use a method on an object that has not been instantiated.

### Causes of NullPointerException in Collectors.toMap
When using Collectors.toMap with null entry values, it may throw a NullPointerException. This is because the method does not allow for null values in the map, as null values would cause the map to become corrupted. Additionally, the method does not check for null values before adding them to the map, which can lead to a NullPointerException.

### Solutions
To avoid a NullPointerException when using Collectors.toMap with null entry values, it is important to check for null values before adding them to the map. Additionally, it is important to use a method that allows for null values, such as the putIfAbsent method, which ensures that the value is only added if it is not null. Finally, it is important to handle any exceptions that may be thrown when attempting to add a null value to the map.
