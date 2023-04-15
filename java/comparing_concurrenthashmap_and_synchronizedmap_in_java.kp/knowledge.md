---
title: How do concurrenthashmap and collections.synchronizedmap(map) differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: ConcurrentHashMap provides better scalability and performance than synchronizedMap, as it allows for concurrent reads and writes without the need for external synchronization.
---

**Contents**

[TOC]

1. **Thread Safety**
    - ConcurrentHashMap is thread-safe and does not need to be externally synchronized. 
    - Collections.synchronizedMap(Map) is not thread-safe and requires external synchronization.

2. **Performance**
    - ConcurrentHashMap is more performant than Collections.synchronizedMap(Map) due to its thread-safety.
    - Collections.synchronizedMap(Map) has to acquire a lock every time a thread wants to access the map, leading to a performance overhead.

3. **API**
    - ConcurrentHashMap provides additional methods like putIfAbsent(), replace(), remove(), etc.
    - Collections.synchronizedMap(Map) does not provide any additional methods.

4. **Implementation**
    - ConcurrentHashMap is implemented using a hash table and multiple locks.
    - Collections.synchronizedMap(Map) is implemented using a synchronized wrapper around the specified map.
