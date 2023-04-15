---
title: How do HashMap and Hashtable in Java differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: HashMap is not synchronized, allows null values, and is not thread-safe, while Hashtable is synchronized, does not allow null values, and is thread-safe.
---

**Contents**

[TOC]

### Thread Safety
HashMap is not thread safe, while Hashtable is thread safe.

### Synchronization
HashMap is non-synchronized, while Hashtable is synchronized.

### Null Keys and Values
HashMap allows one null key and multiple null values, while Hashtable does not allow null keys and values.

### Performance
HashMap is generally faster than Hashtable as it is non-synchronized and allows nulls.
