---
title: What is the most efficient way to convert a list of lists into a single list in Java 8?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the flatMap() method to turn a List of Lists into a List.
---

**Contents**

[TOC]

### Using Streams

Java 8 has a powerful Streams API which can be used to turn a List of Lists into a List. The code below shows how this can be done:

```java
List<List<String>> listOfLists = ...;
List<String> list = listOfLists.stream()
                              .flatMap(Collection::stream)
                              .collect(Collectors.toList());
```

The first line creates a Stream of the List of Lists. The second line uses the `flatMap()` method to flatten the Stream and the third line collects the flattened Stream into a List.

### Using for-loops

It is also possible to turn a List of Lists into a List using for-loops. The code below shows how this can be done:

```java
List<List<String>> listOfLists = ...;
List<String> list = new ArrayList<>();
for (List<String> innerList : listOfLists) {
    list.addAll(innerList);
}
```

The first line creates a List of Lists. The second line creates a new List. The third line iterates over the List of Lists and adds each element of the inner Lists to the new List.

### Using Java 8 Streams and for-loops

It is also possible to combine the Streams API with for-loops to turn a List of Lists into a List. The code below shows how this can be done:

```java
List<List<String>> listOfLists = ...;
List<String> list = new ArrayList<>();
listOfLists.stream()
           .forEach(innerList -> list.addAll(innerList));
```

The first line creates a List of Lists. The second line creates a new List. The third line uses the `forEach()` method to iterate over the List of Lists and add each element of the inner Lists to the new List.

### Using Java 8 Streams, for-loops and Collectors

It is also possible to combine the Streams API, for-loops and Collectors to turn a List of Lists into a List. The code below shows how this can be done:

```java
List<List<String>> listOfLists = ...;
List<String> list = listOfLists.stream()
                              .flatMap(Collection::stream)
                              .collect(Collectors.toList());
```

The first line creates a Stream of the List of Lists. The second line uses the `flatMap()` method to flatten the Stream. The third line collects the flattened Stream into a List.
