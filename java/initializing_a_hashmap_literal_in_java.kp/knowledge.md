---
title: What is the literal syntax for creating a hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can initialize a HashMap in a literal way using the syntax `Map<K, V> map = new HashMap<>() {{ put(K1, V1); put(K2, V2); ... }};`.
---

**Contents**

[TOC]

### Creating a HashMap

A HashMap can be created in Java by instantiating a HashMap object with the following syntax:

```java
HashMap<KeyType, ValueType> hashMapObject = new HashMap<>();
```

### Adding Entries to the HashMap

Entries can be added to the HashMap using the `put` method. The syntax for this is as follows:

```java
hashMapObject.put(key, value);
```

### Initializing a HashMap with Entries

The HashMap can be directly initialized with entries using the following syntax:

```java
HashMap<KeyType, ValueType> hashMapObject = new HashMap<KeyType, ValueType>() {{
    put(key1, value1);
    put(key2, value2);
    // ...
}};
```

### Using Java 8

In Java 8, the HashMap can be initialized with entries using the `of` static method:

```java
HashMap<KeyType, ValueType> hashMapObject = HashMap.of(key1, value1, key2, value2, ...);
```
