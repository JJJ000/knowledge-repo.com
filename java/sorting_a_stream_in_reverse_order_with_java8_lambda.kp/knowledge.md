---
title: What is the syntax for sorting a stream in java8 using a lambda expression in reverse order?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Comparator.reverseOrder() method to sort a stream in reverse order using a Java8 lambda.
---

**Contents**

[TOC]

1. Create a Comparator 

```java
Comparator<Object> reverseOrder = (obj1, obj2) -> obj2.compareTo(obj1);
```

2. Create a Stream

```java
Stream<Object> stream = Stream.of(obj1, obj2, obj3, ...);
```

3. Sort Stream

```java
stream.sorted(reverseOrder);
```

4. Collect Stream

```java
List<Object> sortedList = stream.collect(Collectors.toList());
```
