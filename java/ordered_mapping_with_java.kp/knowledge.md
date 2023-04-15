---
title: Java map with ordering
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: An ordered map is a type of Map in Java that maintains the order of the elements according to their insertion order.
---

**Contents**

[TOC]

### Definition
An ordered map is a type of data structure that stores key-value pairs in a specific order. It is similar to a regular map, except that the order in which elements are stored is determined by the user. This allows for faster retrieval of elements, as the elements are stored in the same order as they were inserted.

### Benefits
The main benefit of using an ordered map is that it allows for faster retrieval of elements. Since the elements are stored in the same order as they were inserted, the time it takes to search for a specific element is much shorter than with a regular map. Additionally, an ordered map can be used to store data in a specific order, which can be useful for sorting and organizing data.

### Java Implementation
In Java, an ordered map is implemented using a TreeMap. A TreeMap is a type of Map that stores its elements in a sorted order. It uses a red-black tree to store the elements, which ensures that the elements are stored in a specific order. Additionally, a TreeMap provides methods for retrieving elements in a specific order, such as retrieving the first element or the last element.

### Usage
An ordered map can be used in a variety of situations, such as sorting data or storing data in a specific order. For example, an ordered map can be used to store a list of students and their grades in order from highest to lowest. Additionally, an ordered map can be used to store elements in a specific order, such as a list of products sorted from lowest price to highest price.
