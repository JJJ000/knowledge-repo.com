---
title: What importance does the load factor have in a hashmap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The load factor determines how full the HashMap is allowed to get before it is resized to reduce the number of collisions.
---

**Contents**

[TOC]

#### Definition
Load factor is a measure of how full the hash table is allowed to get before its capacity is automatically increased. It is a measure of the utilization of the hash table’s buckets.

#### Formula
Load factor is calculated by dividing the number of elements in the hash table by the size of the hash table.

#### Default Value
The default load factor of a Java HashMap is 0.75.

#### Impact
The load factor affects the performance of a HashMap. If the load factor is too low, the HashMap may have to be resized frequently, which can be costly. On the other hand, if the load factor is too high, it can lead to collisions, which can also impact performance.
