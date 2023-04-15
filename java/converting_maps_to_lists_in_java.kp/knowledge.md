---
title: What is the process for transforming a map into a list in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the entrySet() method of the Map interface to convert a Map to a List.
---

**Contents**

[TOC]

### Option 1
1. Create a `List` to store the map entries.
2. Use `Map.entrySet()` to get a set view of the mappings contained in the map.
3. Use `Iterator` to iterate over the set elements and add the elements to the List.

### Option 2
1. Use `Map.keySet()` to get a set view of the keys contained in the map.
2. Use `Iterator` to iterate over the set elements and add the elements to the List.
3. Use `Map.get()` to get the value associated with each key and add the value to the List.
