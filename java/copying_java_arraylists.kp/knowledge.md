---
title: Duplicating a Java arraylist
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The ArrayList class provides a built-in method, clone(), that can be used to copy an ArrayList.
---

**Contents**

[TOC]

# Shallow Copy
A shallow copy of an ArrayList creates a new ArrayList object with the same elements as the original ArrayList. The new ArrayList object is independent of the original, but the elements are not. The elements of the new ArrayList object are the same objects as the elements in the original ArrayList.

# Deep Copy
A deep copy of an ArrayList creates a new ArrayList object with the same elements as the original ArrayList. The new ArrayList object is independent of the original, and the elements are also independent copies of the original elements. The elements of the new ArrayList object are copies of the objects in the original ArrayList.

# Using clone()
The clone() method of the ArrayList class can be used to create a shallow copy of an ArrayList. The clone() method creates a new ArrayList object with the same elements as the original ArrayList. The new ArrayList object is independent of the original, but the elements are not. The elements of the new ArrayList object are the same objects as the elements in the original ArrayList.

# Using Constructor
The constructor of the ArrayList class can be used to create a deep copy of an ArrayList. The constructor creates a new ArrayList object with the same elements as the original ArrayList. The new ArrayList object is independent of the original, and the elements are also independent copies of the original elements. The elements of the new ArrayList object are copies of the objects in the original ArrayList.
