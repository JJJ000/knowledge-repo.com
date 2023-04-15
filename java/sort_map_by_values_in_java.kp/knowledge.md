---
title: How to sort a `map<key, value>` according to values
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can sort a `Map<Key, Value>` by values in Java using a TreeMap, which orders its entries based on their values.
---

**Contents**

[TOC]

### Option 1

1. Create a `List` of `Map.Entry` objects.
2. Create a `Comparator` to sort the `List` by values.
3. Use `Collections.sort()` to sort the `List`.
4. Create a `LinkedHashMap` to store the entries in the sorted order.

### Option 2

1. Create a `Stream` of `Map.Entry` objects.
2. Use `Collectors.toMap()` to convert the `Stream` to a `Map` with the entries sorted by values.
