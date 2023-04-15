---
title: A simple method for transforming an iterable into a collection
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Collection constructor to convert an Iterable to a Collection.
---

**Contents**

[TOC]

### Using Streams

One way to convert an Iterable to a Collection is to use Streams. Streams provide a convenient way to process collections of elements and can be used to convert an Iterable to a Collection. The following code snippet shows how to use Streams to convert an Iterable to a Collection:

```
Iterable<Integer> iterable = ...;
Collection<Integer> collection = StreamSupport.stream(iterable.spliterator(), false)
        .collect(Collectors.toList());
```

### Using for-each Loop

Another way to convert an Iterable to a Collection is to use a for-each loop. The following code snippet shows how to use a for-each loop to convert an Iterable to a Collection:

```
Iterable<Integer> iterable = ...;
Collection<Integer> collection = new ArrayList<>();
for (Integer i : iterable) {
    collection.add(i);
}
```

### Using Java 8 Streams

Java 8 Streams can also be used to convert an Iterable to a Collection. The following code snippet shows how to use Java 8 Streams to convert an Iterable to a Collection:

```
Iterable<Integer> iterable = ...;
Collection<Integer> collection = StreamSupport.stream(iterable.spliterator(), false)
        .collect(Collectors.toList());
```

### Using Java 9 Streams

Java 9 Streams can also be used to convert an Iterable to a Collection. The following code snippet shows how to use Java 9 Streams to convert an Iterable to a Collection:

```
Iterable<Integer> iterable = ...;
Collection<Integer> collection = StreamSupport.stream(iterable.spliterator(), false)
        .collect(Collectors.toCollection(ArrayList::new));
```
