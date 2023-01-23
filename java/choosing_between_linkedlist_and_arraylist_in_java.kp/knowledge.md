---
title: What are the advantages of using a linkedlist over an arraylist in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: LinkedList should be used when frequent insertion and deletion operations need to be performed, as it offers faster performance than ArrayList.
---

**Contents**

[TOC]

### When Insertion and Deletion is Frequent
LinkedList is more efficient than ArrayList when insertion and deletion of elements is frequent, because in LinkedList the elements are not stored in contiguous memory locations, so adding and removing elements does not require shifting of elements.

### When Memory is Limited
LinkedList is more memory efficient than ArrayList because it does not need to allocate memory for all its elements at once, as it only stores the address of the next element.

### When Random Access is Not Required
LinkedList is preferred over ArrayList when random access is not required, as LinkedList does not provide random access to its elements.

### When Iteration is Required
LinkedList is preferred over ArrayList when iteration is required, as LinkedList provides faster iteration than ArrayList.
