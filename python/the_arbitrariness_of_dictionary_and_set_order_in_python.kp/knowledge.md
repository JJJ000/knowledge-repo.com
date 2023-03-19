---
title: What makes the order of dictionaries and sets arbitrary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The order is arbitrary in dictionaries and sets in Python because they are implemented as hash tables, which do not have a predictable order.
---

**Contents**

[TOC]

## Introduction
In Python, dictionaries and sets are two important built-in data structures. These two data structures have some characteristics in common, particularly that both are implemented using hash tables. However, one of the noticeable differences between them is that their order is arbitrary. This means that the order in which elements are inserted into a dictionary or set is not preserved. In this article, we will explore the reasons why the order is arbitrary in these structures.

## Hash Tables
Both dictionaries and sets in Python are implemented using hash tables. A hash table is a data structure that allows us to store and retrieve values based on keys. Each value is associated with a unique key, which is used to index the value in the hash table. The Python interpreter uses hash tables to store dictionary and set objects. 

In a hash table, the keys are hashed to generate an index into an array of buckets or slots. The value is then stored in the bucket at that index. The hash function that is used to generate the index is designed to spread the keys evenly across the array to minimize collisions. However, collisions can still occur when two keys hash to the same index. When a collision happens, the hash table uses a technique called chaining to store the values in a linked list. 

In Python, dictionaries and sets use dynamically-sized hash tables that automatically resize as more items are added. This allows them to be very efficient for lookups, insertions, and deletions.

## Arbitrary Order
One consequence of using hash tables to implement dictionaries and sets is that the order in which elements are inserted is not preserved. This is because the hash function used to generate the index is not dependent on the order of insertion. 

For dictionaries, this means that the order of the keys is arbitrary. If we create a dictionary and insert some keys and values, we cannot assume that the keys will be in the same order we inserted them:

```python
>>> d = {}
>>> d['a'] = 1
>>> d['c'] = 3
>>> d['b'] = 2
>>> print(d)
{'a': 1, 'b': 2, 'c': 3}
```

For sets, the order of the elements is also arbitrary. If we create a set and insert some elements, we cannot assume that the elements will be in the same order we inserted them:

```python
>>> s = set()
>>> s.add('a')
>>> s.add('c')
>>> s.add('b')
>>> print(s)
{'a', 'c', 'b'}
```

## Why Arbitrary Order?
The reason why the order of dictionaries and sets is arbitrary in Python is mainly performance-related. By not storing order information, dictionaries and sets can be implemented more efficiently using hash tables. This leads to faster lookups, insertions, and deletions for large datasets.

If order information was stored in dictionaries or sets, it would require extra memory and computation to maintain that order. This would make dictionary and set operations slower and less memory-efficient. Additionally, keeping the order information up-to-date would make it more difficult to implement dynamically-sized hash tables.

## Conclusion
In conclusion, the order of elements in dictionaries and sets is arbitrary in Python because they are implemented using hash tables. Hash tables allow for fast lookups, insertions, and deletions by not storing order information. If order information was stored, it would require extra memory and computation to maintain, making dictionary and set operations slower and less memory-efficient.
