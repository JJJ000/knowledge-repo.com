---
title: What is the reason that java.util.set does not have a get(int index) method?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Java.util.Set is an unordered collection that does not support indexed access.
---

**Contents**

[TOC]

1. Overview
Java.util.Set is an interface that extends the Java Collection interface. It is an unordered collection of elements and does not allow duplicate elements.

2. Difference between Set and List
The main difference between Set and List is that Set does not allow duplicate elements while List allows duplicate elements. Additionally, Set does not maintain the order of the elements while List does.

3. Why Set does not have get(int index)
Since Set does not maintain the order of the elements, it does not provide a way to access elements by index. Accessing elements by index is only possible in List since it maintains the order of the elements.
