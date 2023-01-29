---
title: How can I use Java 8 to quickly loop through a stream and keep track of the index?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, you can use the forEachOrdered() method with an indexed lambda expression.
---

**Contents**

[TOC]

1. Using Stream.forEach():

This method allows us to iterate over a Stream with indices in Java 8. It takes a BiConsumer as an argument, which is a functional interface that takes two arguments and returns no result. The first argument is the index of the element in the Stream, and the second argument is the element itself.

```
IntStream.range(0, list.size())
        .forEach(i -> System.out.println("Index: " + i + " Value: " + list.get(i)));
```

2. Using Stream.map():

The map() method can be used to convert a Stream into a Stream of objects that contain both an index and the element itself. This allows us to iterate over the Stream with indices in a concise way.

```
list.stream()
    .map(e -> new IndexedElement(list.indexOf(e), e))
    .forEach(System.out::println);
```

3. Using Stream.collect():

The collect() method can be used to collect the elements of a Stream into a List. This allows us to iterate over the List with indices in a concise way.

```
List<IndexedElement> indexedElements = list.stream()
                                          .map(e -> new IndexedElement(list.indexOf(e), e))
                                          .collect(Collectors.toList());

indexedElements.forEach(System.out::println);
```

4. Using Stream.reduce():

The reduce() method can be used to accumulate the elements of a Stream into a single object. This allows us to iterate over the Stream with indices in a concise way.

```
IndexedElement result = list.stream()
                            .reduce(new IndexedElement(0, null),
                                    (acc, e) -> new IndexedElement(list.indexOf(e), e));

System.out.println(result);
```
