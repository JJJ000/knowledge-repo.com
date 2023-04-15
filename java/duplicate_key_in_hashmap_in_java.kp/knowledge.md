---
title: What occurs when a key that already exists in a hashmap is added again?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The value associated with the duplicate key will be overwritten.
---

**Contents**

[TOC]

### Overwriting
When a duplicate key is put into a HashMap in Java, the value associated with the key is overwritten. The original value for the key is replaced with the new value. 

### Duplicate Keys
The HashMap does not recognize duplicate keys, so the duplicate key is treated as a new key and the new value is associated with it.

### Performance
The HashMap structure is designed to have constant time complexity for basic operations like get and put. Therefore, the performance of the HashMap is unaffected by the presence of duplicate keys. 

### Collision Handling
The HashMap uses a hashing algorithm to store and retrieve elements. In case of a collision (i.e. when two keys have the same hash value), the HashMap uses a linked list to store the elements with the same hash value. When a duplicate key is put into the HashMap, the linked list is traversed to find the element with the same key and the value is overwritten.
