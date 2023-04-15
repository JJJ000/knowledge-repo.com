---
title: What is the method for retrieving a key from a value in a Java hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `get()` method to retrieve the key associated with a given value in a Hashmap.
---

**Contents**

[TOC]

### Using EntrySet

The `entrySet()` method of `HashMap` class is used to return a set view of the mappings present in the map. This method returns a `Set` of `Map.Entry` object which is having methods to get the key and value.

The following example shows how to get the key from value using `entrySet()` method.

```java
HashMap<String, Integer> map = new HashMap<>();
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);

for (Map.Entry<String, Integer> entry : map.entrySet()) {
    if (entry.getValue().equals(2)) {
        System.out.println("Key for value 2 is: " + entry.getKey());
    }
}
```

### Using Stream API

Java 8 introduced the `Stream` API which provides a powerful facility to process data in a declarative manner.

The following example shows how to get the key from value using `Stream` API.

```java
HashMap<String, Integer> map = new HashMap<>();
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);

Optional<String> key = map.entrySet().stream()
        .filter(e -> e.getValue().equals(2))
        .map(Map.Entry::getKey)
        .findFirst();

System.out.println("Key for value 2 is: " + key.orElse(null));
```

### Using Lambda Expression

Java 8 also introduced Lambda expressions which provides a concise way to represent the anonymous functions.

The following example shows how to get the key from value using Lambda expression.

```java
HashMap<String, Integer> map = new HashMap<>();
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);

String key = map.entrySet().stream()
        .filter(e -> e.getValue().equals(2))
        .map(Map.Entry::getKey)
        .findFirst()
        .orElse(null);

System.out.println("Key for value 2 is: " + key);
```
