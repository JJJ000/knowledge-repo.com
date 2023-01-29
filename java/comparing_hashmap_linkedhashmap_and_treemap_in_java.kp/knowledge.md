---
title: What are the distinctions between hashmap, linkedhashmap, and treemap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: HashMap stores key-value pairs in no particular order, LinkedHashMap stores key-value pairs in the order they were inserted, and TreeMap stores key-value pairs in natural order of the keys.
---

**Contents**

[TOC]

### HashMap
HashMap is an implementation of the Map interface that uses a hash table for storage. It stores key-value pairs and is generally considered the fastest implementation of the Map interface. It does not preserve the insertion order of the elements.

### LinkedHashMap
LinkedHashMap is an implementation of the Map interface that uses a hash table and linked list. It stores key-value pairs and preserves the insertion order of the elements. It is slower than HashMap but faster than TreeMap.

### TreeMap
TreeMap is an implementation of the Map interface that uses a red-black tree for storage. It stores key-value pairs and preserves the natural ordering of the elements. It is slower than HashMap and LinkedHashMap.
