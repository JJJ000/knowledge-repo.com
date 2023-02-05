---
title: Using stream transform the hashmap<x, y> to a stream of entries, then use the stream.map() method to map each entry to a new entry with the same key and a different value, and finally use the stream.collect() method to collect the new entries into a new hashmap<x, z>.

using map-reduce use a map-reduce operation to transform the hashmap<x, y> into a new hashmap<x, z>. the map phase would iterate over each entry in the original hashmap and create a new entry with the same key and a different value. the reduce phase would then collect the new entries into a new hashmap.

using collector define a collector which will iterate over each entry in the original hashmap and create a new entry with the same key and a different value, and then collect the new entries into a new hashmap<x, z>
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Using Stream and Map-Reduce or Collector, one can transform a HashMap<X, Y> to a HashMap<X, Z> by mapping each entry to a new value Z.
---

**Contents**

[TOC]

### Map-Reduce
The Map-Reduce approach involves mapping each element of the original HashMap into a new element and then reducing the mapped elements into a new HashMap. 

The mapping step can be done using Streams, which allows us to iterate over each element in the original HashMap and create a new element with a different value.

For example, we can map each element from a HashMap<String, Integer> to a HashMap<String, String> by using the Stream.map() method:

```
HashMap<String, String> newMap = oldMap.entrySet().stream()
    .map(entry -> new AbstractMap.SimpleEntry<>(entry.getKey(), entry.getValue().toString()))
    .collect(Collectors.toMap(Map.Entry::getKey, Map.Entry::getValue));
```

### Collector
The Collector approach is similar to the Map-Reduce approach, but it uses a Collector to collect the mapped elements into a new HashMap.

The Collector can be used to collect the mapped elements into a new HashMap by using the Collectors.toMap() method.

For example, we can collect the mapped elements from a HashMap<String, Integer> to a HashMap<String, String> by using the Collectors.toMap() method:

```
HashMap<String, String> newMap = oldMap.entrySet().stream()
    .collect(Collectors.toMap(
        Map.Entry::getKey, 
        entry -> entry.getValue().toString()));
```
