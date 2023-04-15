---
title: Obtaining an array from a java.util.stream.stream in Java 8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Stream`s collect() method to retrieve a List from a Stream.
---

**Contents**

[TOC]

### Creating a Stream

A Stream in Java 8 can be created from a variety of sources. The most common sources are collections, arrays, and generator functions. 

To create a Stream from a collection, use the `stream()` or `parallelStream()` methods of the collection interface. For example, to create a Stream from a List, use the `list.stream()` or `list.parallelStream()` methods.

To create a Stream from an array, use the `Arrays.stream(array)` method.

To create a Stream from a generator function, use the `Stream.generate(Supplier s)` or `Stream.iterate(T seed, UnaryOperator f)` methods.

### Retrieving a List from a Stream

Once a Stream has been created, a List can be retrieved from it using the `collect()` method. The `collect()` method requires a `Collector` as a parameter. To retrieve a List from a Stream, use the `Collectors.toList()` method.

For example, to retrieve a List from a Stream of strings, use the following code:

```java
List<String> list = stream.collect(Collectors.toList());
```

### Processing a Stream

Before retrieving a List from a Stream, the Stream may need to be processed. Processing a Stream involves applying operations to the elements of the Stream. Common operations include filtering, mapping, and sorting.

To filter a Stream, use the `filter(Predicate p)` method. To map a Stream, use the `map(Function f)` method. To sort a Stream, use the `sorted(Comparator c)` method.

### Example

The following example creates a Stream from a List, processes the Stream, and retrieves a List from the Stream:

```java
List<String> list = Arrays.asList("a", "b", "c", "d");

List<String> result = list.stream()
    .filter(s -> s.startsWith("b"))
    .map(String::toUpperCase)
    .sorted()
    .collect(Collectors.toList());
```

In this example, the Stream is filtered to only include elements starting with "b", mapped to upper case, sorted, and then collected into a List. The resulting List will contain the element "B".
