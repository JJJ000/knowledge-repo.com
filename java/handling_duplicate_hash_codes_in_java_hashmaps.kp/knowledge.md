---
title: What happens when multiple objects have the same hash code in a Java hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: It uses an internal linked list to store objects with the same hash code.
---

**Contents**

[TOC]

# Collision Resolution
A Java HashMap handles different objects with the same hash code by using collision resolution. When a HashMap is created, each key is assigned a hash code. If two keys have the same hash code, a collision occurs. To handle this, the HashMap uses a technique called chaining. In chaining, each hash code is associated with a linked list of entries. When a collision occurs, the entry is added to the linked list associated with the hash code. 

# Performance
Chaining has the advantage of being able to handle collisions without sacrificing too much performance. When a key is added to the HashMap, it is compared to the keys in the linked list associated with the hash code. If the key is already present, the associated value is replaced. Otherwise, the key and its associated value are added to the linked list. This process is faster than having to re-hash all the keys in the HashMap when a collision occurs.

# Advantages
Chaining also has the advantage of being able to handle a large number of entries with the same hash code. This is because the linked list associated with the hash code can grow as needed. This means that the HashMap can handle a large number of entries without having to re-hash them.

# Disadvantages
The main disadvantage of chaining is that it can result in a large number of entries in the linked list associated with a single hash code. This can lead to poor performance when searching for a specific key. Additionally, chaining can lead to a large amount of memory being used to store the linked lists.
