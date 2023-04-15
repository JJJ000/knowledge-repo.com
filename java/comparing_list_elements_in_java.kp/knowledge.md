---
title: What is the easiest method to determine if two separate lists have the same elements?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Comparing the two lists using the equals() method will determine if they contain the same elements.
---

**Contents**

[TOC]

### Solution 1: Using HashSet

1. Create two HashSet objects, one for each list.
2. Add all the elements of the two lists to their respective HashSet objects.
3. Compare the two HashSet objects. If they are equal, then the two lists contain exactly the same elements.

### Solution 2: Using Arrays

1. Convert both lists to arrays.
2. Sort the arrays.
3. Compare the sorted arrays. If they are equal, then the two lists contain exactly the same elements.
