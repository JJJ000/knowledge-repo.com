---
title: Checking if a key exists in a hashmap
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The containsKey() method can be used to check if a key exists in a HashMap.
---

**Contents**

[TOC]

### Using `containsKey()`
The `containsKey()` method of the `java.util.HashMap` class can be used to check if a key exists in the HashMap or not. It returns `true` if the key exists in the map, otherwise it returns `false`.

**Example**
```
HashMap<String, Integer> map = new HashMap<>();
map.put("one", 1);
map.put("two", 2);

if (map.containsKey("one")) {
    System.out.println("Key exists!");
}
```

### Using `get()`
The `get()` method of the `java.util.HashMap` class can also be used to check if a key exists in the HashMap or not. It returns the value associated with the key if the key exists in the map, otherwise it returns `null`.

**Example**
```
HashMap<String, Integer> map = new HashMap<>();
map.put("one", 1);
map.put("two", 2);

if (map.get("one") != null) {
    System.out.println("Key exists!");
}
```
