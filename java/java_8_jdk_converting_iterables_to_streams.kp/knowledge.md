---
title: Use the Java 8 jdk to turn an iterable into a stream
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Stream.of() method to convert an Iterable to a Stream in Java 8.
---

**Contents**

[TOC]

### Introduction

Java 8 introduced the Stream API, which provides a convenient way to work with collections of objects. Streams allow you to process data in a declarative way, making it easier to read and maintain code. Streams can be used to convert an Iterable object into a Stream. 

### Creating a Stream from Iterable

To create a Stream from an Iterable, you can use the `stream()` method provided by the Iterable interface. This method returns a Stream object that can be used to process the data in the Iterable. The following example shows how to create a Stream from an ArrayList:

```java
List<String> list = new ArrayList<>();
list.add("foo");
list.add("bar");

Stream<String> stream = list.stream();
```

### Processing the Stream

Once you have created a Stream from an Iterable, you can use the various Stream methods to process the data. For example, you can use the `map()` method to apply a transformation to each element in the Stream:

```java
Stream<String> newStream = stream.map(String::toUpperCase);
```

You can also use the `filter()` method to filter out elements that do not match a certain criteria:

```java
Stream<String> filteredStream = stream.filter(s -> s.length() > 3);
```

### Collecting the Stream

Once you have processed the Stream, you can use the `collect()` method to collect the elements into a new collection. For example, you can use the `toList()` method to collect the Stream into a List:

```java
List<String> newList = newStream.collect(Collectors.toList());
```

You can also use other methods such as `toSet()` and `toMap()` to collect the Stream into different types of collections.
