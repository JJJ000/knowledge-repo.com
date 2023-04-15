---
title: What distinctions exist between arraylist and vector?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: ArrayList is non-synchronized, whereas Vector is synchronized.
---

**Contents**

[TOC]

### Memory Allocation
ArrayList is non-synchronized and can be resized dynamically. Vector is synchronized and grows in size by doubling its current size.

### Performance
ArrayList is faster than Vector as it is non-synchronized. Vector operations are thread-safe and can be used in multi-threaded environment, but the performance is low.

### Capacity
ArrayList has no default capacity. Vector has a default capacity of 10.

### Methods
ArrayList provides methods like add(), remove(), contains(), get(), set(), etc. Vector provides methods like addElement(), removeElement(), elementAt(), etc.
