---
title: What is the most effective way to transform a list in Java 8 using the map or foreach function?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The best way to transform a list in Java 8 is to use the Stream.map() method.
---

**Contents**

[TOC]

### Map
The `map()` method is a convenient way to transform a list of elements in Java 8. The `map()` method takes a `Function` as an argument, which is applied to each element in the list and returns a new list with the transformed elements. For example, the following code will double each element in the list: 

```java
List<Integer> list = Arrays.asList(1, 2, 3);
List<Integer> doubledList = list.stream()
    .map(x -> x * 2)
    .collect(Collectors.toList());
```

### ForEach
The `forEach()` method is another way to transform a list of elements in Java 8. The `forEach()` method takes a `Consumer` as an argument, which is applied to each element in the list. For example, the following code will double each element in the list: 

```java
List<Integer> list = Arrays.asList(1, 2, 3);
list.forEach(x -> x *= 2);
```

### Comparison
The main difference between `map()` and `forEach()` is that `map()` returns a new list with the transformed elements, while `forEach()` modifies the existing list. Therefore, `map()` is more suitable for transforming a list when the original list needs to be preserved.

### Conclusion
In Java 8, the `map()` and `forEach()` methods are two convenient ways to transform a list of elements. `map()` is better suited for transforming a list when the original list needs to be preserved, while `forEach()` is better suited for transforming a list when the original list can be modified.
