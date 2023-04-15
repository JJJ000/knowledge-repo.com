---
title: A Java class that implements a map and maintains the order of elements as they were inserted
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: LinkedHashMap is a Java Class that implements Map and keeps insertion order.
---

**Contents**

[TOC]

### LinkedHashMap
LinkedHashMap is a class that implements the Map interface and it maintains the insertion order of the elements. It is a combination of a HashMap and a LinkedList. It stores the elements in the order in which they are inserted. It maintains a doubly-linked list running through all of its entries. This linked list defines the iteration order, which is normally the order in which keys were inserted into the map.

### Constructors
LinkedHashMap provides one constructor that creates an empty map:
```java
LinkedHashMap<K,V> linkedHashMap = new LinkedHashMap<>();
```
It also provides several more constructors that allow you to specify the initial capacity, load factor, and ordering mode of the map.

### Advantages
LinkedHashMap has several advantages over a HashMap. First, it maintains the insertion order of the elements. Second, it has faster iteration than a HashMap, since the elements are stored in a linked list. Third, it is thread-safe, since it is backed by a synchronized Map. Finally, it allows null values and null keys.

### Disadvantages
The main disadvantage of LinkedHashMap is that it uses more memory than a HashMap, since it stores the elements in a doubly-linked list. Additionally, it is slower than a HashMap, since it has to traverse the linked list to find an element.
