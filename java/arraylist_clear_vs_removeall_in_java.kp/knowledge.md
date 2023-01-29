---
title: How do arraylist.clear() and arraylist.removeall() differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: ArrayList.clear() removes all elements from the list, while ArrayList.removeAll() removes all elements from the list that are contained in a specified collection.
---

**Contents**

[TOC]

### ArrayList.clear()
ArrayList.clear() removes all elements from the list. It is a fast operation, since it does not involve any comparison or allocation of memory.

### ArrayList.removeAll()
ArrayList.removeAll() removes all elements from the list that are contained in a specified collection. This operation requires comparison and memory allocation.
