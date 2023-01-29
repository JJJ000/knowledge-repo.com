---
title: What is the reason for the absence of a sortedlist in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: SortedList is not necessary in Java because its collections framework provides other sorting options.
---

**Contents**

[TOC]

### Reasons for Lack of SortedList

### Unnecessary Complexity
A SortedList would add unnecessary complexity to the Java Collections API.  It would require additional methods for sorting and maintaining the sorted order, as well as additional overhead for maintaining the sorting order.

### Unnecessary Duplication
A SortedList would also add unnecessary duplication to the Java Collections API. Java already provides the TreeSet and TreeMap classes for maintaining sorted collections.

### Limited Use Cases
Finally, the use cases for a SortedList are limited. In most cases, the sorting order of a collection is not important and a regular list is sufficient. When sorting is important, a TreeSet or TreeMap is usually more appropriate.
