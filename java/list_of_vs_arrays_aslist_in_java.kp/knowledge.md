---
title: What are the distinctions between list.of and arrays.aslist?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: List.of creates an immutable list, whereas Arrays.asList creates a list that is backed by the original array, which can be modified.
---

**Contents**

[TOC]

1. **Return Type:**
List.of() returns an immutable List, while Arrays.asList() returns a List that is backed by the original array.

2. **Modification:**
List.of() returns a List that cannot be modified, while Arrays.asList() returns a List that can be modified.

3. **Number of Elements:**
List.of() can accept any number of elements, while Arrays.asList() accepts only an array of elements.

4. **Performance:**
List.of() is faster than Arrays.asList() since it does not need to create a new List. Arrays.asList() has to create a new List from the array, which can take more time.
