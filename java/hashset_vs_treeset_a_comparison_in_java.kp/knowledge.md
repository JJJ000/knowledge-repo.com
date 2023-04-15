---
title: Comparing hashset and treeset
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: HashSet is a collection that uses a hash table for storage, while TreeSet is a collection that stores its elements in a sorted tree structure.
---

**Contents**

[TOC]

### HashSet
HashSet is a part of the Java Collection framework. It implements the Set interface. It is an unordered collection of objects in which duplicate values cannot be stored. Just like HashMap, HashSet uses a hash table for storage.

### TreeSet
TreeSet is a part of the Java Collection framework. It implements the SortedSet interface. It is an ordered collection of objects in which duplicate values cannot be stored. Just like TreeMap, TreeSet uses a tree structure for storage.

### Differences
1. HashSet is unordered while TreeSet is ordered.
2. HashSet does not guarantee that the order of the elements will remain constant over time while TreeSet does.
3. HashSet allows the storage of null elements while TreeSet does not.
4. HashSet is faster than TreeSet while TreeSet provides a total ordering of the elements.
