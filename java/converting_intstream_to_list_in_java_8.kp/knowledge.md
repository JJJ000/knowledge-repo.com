---
title: What is the process for transforming a Java 8 intstream into a list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the IntStream`s collect() method with a Collector that accumulates the elements into a List.
---

**Contents**

[TOC]

### Using Collectors

The `collect()` method of the `IntStream` interface can be used to convert an `IntStream` to a `List`. The `collect()` method takes a `Collector` as an argument which is used to accumulate the input elements into a mutable result container.

The following code snippet shows how to convert an `IntStream` to a `List` using the `Collectors.toList()` method:

```java
List<Integer> intList = intStream.collect(Collectors.toList());
```

### Using Stream.mapToObj()

The `mapToObj()` method of the `IntStream` interface can also be used to convert an `IntStream` to a `List`. The `mapToObj()` method takes a `IntFunction` as an argument which is used to convert the `IntStream` elements to `Object`s.

The following code snippet shows how to convert an `IntStream` to a `List` using the `mapToObj()` method:

```java
List<Integer> intList = intStream.mapToObj(Integer::valueOf).collect(Collectors.toList());
```

### Using Stream.boxed()

The `boxed()` method of the `IntStream` interface can also be used to convert an `IntStream` to a `List`. The `boxed()` method takes no arguments and returns a `Stream` of boxed `Integer`s.

The following code snippet shows how to convert an `IntStream` to a `List` using the `boxed()` method:

```java
List<Integer> intList = intStream.boxed().collect(Collectors.toList());
```
