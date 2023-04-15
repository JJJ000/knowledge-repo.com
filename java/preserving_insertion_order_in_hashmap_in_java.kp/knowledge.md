---
title: What is the best way to maintain the order of elements in a hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The insertion order in HashMap can be preserved by using LinkedHashMap instead.
---

**Contents**

[TOC]

### Section 1 - Create a LinkedHashMap

A LinkedHashMap is a type of HashMap that preserves insertion order. It is easy to create a LinkedHashMap in Java by using the following constructor:

`LinkedHashMap<String, String> myMap = new LinkedHashMap<String, String>();`

### Section 2 - Add Elements to the Map

Once the LinkedHashMap has been created, elements can be added to it in the same way as a regular HashMap. For example:

`myMap.put("key1", "value1");`

`myMap.put("key2", "value2");`

### Section 3 - Iterate Through the Map

When iterating through the LinkedHashMap, the elements will be returned in the same order they were inserted. For example:

`for (String key : myMap.keySet()) {`

`    System.out.println(key + ": " + myMap.get(key));`

`}`

### Section 4 - Output

The output of the above code would be:

`key1: value1`

`key2: value2`
