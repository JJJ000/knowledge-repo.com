---
title: What advantages does arraydeque have over linkedlist?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: ArrayDeque is more efficient than LinkedList because it provides constant time performance for add, remove, and get operations.
---

**Contents**

[TOC]

1. Memory Usage:
ArrayDeque requires less memory than LinkedList because it does not have to store references to the previous and next nodes.

2. Performance:
ArrayDeque is faster than LinkedList when it comes to adding and removing elements from the beginning and end of the list. This is because ArrayDeque uses an array to store its elements, while LinkedList uses a doubly linked list.

3. Thread Safety:
ArrayDeque is not thread-safe, while LinkedList is thread-safe. This means that multiple threads can access and modify a LinkedList without any issues, while ArrayDeque must be synchronized manually in order to be thread-safe.

4. Iteration:
ArrayDeque allows for fast iteration over its elements, while LinkedList requires more time to iterate over its elements due to the need to traverse the doubly linked list.
