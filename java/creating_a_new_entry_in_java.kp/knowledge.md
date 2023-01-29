---
title: How to create a new key-value pair in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can create a new Entry (key, value) by using the put() method of a Map.
---

**Contents**

[TOC]

1. **Creating a Map**
Before you can add a new entry (key, value) to a Map, you must first create the Map. To do this, you can use the `HashMap` class which is part of the Java Collections Framework.

2. **Adding Entries**
Once the Map is created, you can add entries using the `put()` method. The syntax for this method is `put(key, value)`. This method takes two arguments, the key and the value, and adds them to the Map.

3. **Retrieving Entries**
Once the entries have been added to the Map, you can retrieve them using the `get()` method. The syntax for this method is `get(key)`. This method takes one argument, the key, and returns the associated value.

4. **Iterating Over Entries**
If you want to iterate over all of the entries in the Map, you can use the `entrySet()` method. This method returns a `Set` of `Map.Entry` objects which can then be iterated over using a `for` loop.
