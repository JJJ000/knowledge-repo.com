---
title: How do the map() and flatmap() methods in Java 8 differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The map() method applies a function to each element in a stream, while the flatMap() method applies a function to each element, and then flattens the results into a single stream.
---

**Contents**

[TOC]

### Map()
The `map()` method is used to transform a stream of objects into another stream of objects. It applies a function to each element of the stream and returns a new stream with the transformed elements.

### FlatMap()
The `flatMap()` method is used to transform a stream of objects into another stream of objects. It applies a function to each element of the stream and returns a new stream with the flattened elements. The elements of the new stream are the result of applying the function to each element of the original stream. Unlike `map()`, `flatMap()` does not return a stream of streams, but instead returns a single stream with all the elements flattened.
