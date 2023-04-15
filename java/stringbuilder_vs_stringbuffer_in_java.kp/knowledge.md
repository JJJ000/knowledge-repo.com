---
title: What are the distinctions between StringBuilder and StringBuffer?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: StringBuilder is not thread-safe, while StringBuffer is thread-safe.
---

**Contents**

[TOC]

### StringBuilder
StringBuilder is a mutable sequence of characters. It is similar to StringBuffer but with no guarantee of synchronization.

### StringBuffer
StringBuffer is a mutable sequence of characters. It is similar to StringBuilder but with a guarantee of synchronization.

### Difference
1. StringBuilder is not synchronized, while StringBuffer is synchronized.
2. StringBuilder is faster than StringBuffer.
3. StringBuilder is preferred over StringBuffer for non-thread applications.
