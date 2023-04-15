---
title: How do hashmap and map objects differ in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: HashMap is an implementation of the Map interface that uses a hash table for storage, while Map is an interface that defines methods for working with key-value mappings.
---

**Contents**

[TOC]

### Major Difference
The major difference between the HashMap and Map objects in Java is that HashMap is an implementation of Map interface while Map is an interface.

### HashMap
HashMap is an implementation of Map interface. It stores the data in key-value pairs and provides constant time complexity for insertion, deletion, and retrieval operations. It is not synchronized and is not thread-safe. It allows one null key and multiple null values.

### Map
Map is an interface. It is used to store the data in key-value pairs. It does not allow duplicate keys but allows duplicate values. It is not synchronized and is not thread-safe. It does not allow null keys and null values.
