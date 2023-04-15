---
title: Search for the first element that meets the criteria
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The first element matching the given predicate can be found using the findFirst() method of the Stream interface.
---

**Contents**

[TOC]

### Introduction

Finding the first element of a sequence that satisfies a predicate is a common task in Java programming. The task can be accomplished using the `Stream` API, which provides a powerful set of methods for processing sequences of objects.

### Stream API

The `Stream` API provides a `findFirst()` method which returns an `Optional` object containing the first element in the stream that satisfies the given predicate. This method takes a `Predicate` object as an argument. A `Predicate` is a functional interface that takes a single argument and returns a boolean value.

### Example

For example, to find the first element of a `List` of `Integer`s that is greater than 10, the following code can be used:

```java
List<Integer> list = Arrays.asList(1, 2, 3, 11, 12, 13);
Optional<Integer> result = list.stream()
    .filter(i -> i > 10)
    .findFirst();
```

### Conclusion

In conclusion, the `Stream` API provides a convenient way to find the first element of a sequence that satisfies a given predicate.
