---
title: What is the implementation of python's built-in dictionaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Python`s built in dictionaries are implemented as hash tables.
---

**Contents**

[TOC]

1. Data Structure #
Python's built-in dictionaries are implemented using a hash table, which is a data structure that uses a key-value pair to store and retrieve data quickly.

2. Hashing #
When a key-value pair is added to a dictionary, the key is hashed using a hash function. The hash value is then used to determine the position in the hash table where the value should be stored.

3. Collision Resolution #
When two keys are hashed to the same position in the hash table, a collision occurs. To handle this, Python uses a technique called chaining, which stores the colliding values in a linked list at the same position in the hash table.

4. Rehashing #
When the number of elements in a dictionary grows, the hash table needs to be resized to ensure that lookups remain fast. This process is called rehashing and involves creating a new hash table with a larger size and rehashing all the elements into the new table.
