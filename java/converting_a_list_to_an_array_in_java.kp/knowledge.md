---
title: Turn a list into an array in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Arrays.asList() method can be used to convert a list to an array in Java.
---

**Contents**

[TOC]

### Using `Object[]`

We can convert a list to an array in Java using the `toArray()` method of the `List` interface. This method takes an `Object[]` as an argument and returns an array of the same type.

```java
List<String> list = new ArrayList<String>();
list.add("a");
list.add("b");
list.add("c");

Object[] array = list.toArray();
```

### Using Generics

We can also use generics to create an array of the same type as the list. This is done using the `toArray(T[] a)` method of the `List` interface.

```java
List<String> list = new ArrayList<String>();
list.add("a");
list.add("b");
list.add("c");

String[] array = list.toArray(new String[list.size()]);
```

### Using Streams

We can also use streams to convert a list to an array. This is done using the `toArray()` method of the `Stream` interface.

```java
List<String> list = new ArrayList<String>();
list.add("a");
list.add("b");
list.add("c");

String[] array = list.stream().toArray(String[]::new);
```

### Using Java 8

We can also use the new Java 8 `Collectors` class to convert a list to an array. This is done using the `toArray()` method of the `Collectors` class.

```java
List<String> list = new ArrayList<String>();
list.add("a");
list.add("b");
list.add("c");

String[] array = list.stream().collect(Collectors.toArray(String[]::new));
```
