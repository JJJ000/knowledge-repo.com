---
title: Transforming an array into a list in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can convert an array to a list in Java by using the Arrays.asList() method.
---

**Contents**

[TOC]

### Using Java 8 Stream

Java 8 Stream API provides a convenient way to convert an array to a list.

```java
String[] array = {"a", "b", "c"};

List<String> list = Arrays.stream(array).collect(Collectors.toList());
```

### Using Java Arrays

The Arrays class provides a static method called asList() to convert an array to a list.

```java
String[] array = {"a", "b", "c"};

List<String> list = Arrays.asList(array);
```

### Using Java List Constructor

Java List interface provides a constructor to create a list from an array.

```java
String[] array = {"a", "b", "c"};

List<String> list = new ArrayList<>(Arrays.asList(array));
```

### Using Java for Loop

We can also use a simple for loop to convert an array to a list.

```java
String[] array = {"a", "b", "c"};

List<String> list = new ArrayList<>();

for (String s : array) {
    list.add(s);
}
```
