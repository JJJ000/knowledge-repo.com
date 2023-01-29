---
title: Which is faster to use in Java an array or a list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: List is generally faster than Array in Java.
---

**Contents**

[TOC]

### Array

### Pros
- Arrays are faster than Lists when retrieving data, as they are indexed and allow direct access to any element.
- Arrays use less memory than Lists, as they are of a fixed size.

### Cons
- Arrays are of a fixed size and cannot be dynamically resized.
- Arrays cannot store different data types in the same array.

### List

### Pros
- Lists are dynamic and can be resized to accommodate more elements.
- Lists can store elements of different data types.

### Cons
- Lists are slower than Arrays when retrieving data, as they are not indexed and require linear search.
- Lists use more memory than Arrays, as they are of a dynamic size.
