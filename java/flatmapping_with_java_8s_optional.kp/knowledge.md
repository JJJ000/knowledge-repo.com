---
title: Utilizing the optional feature in Java 8 with streamflatmap
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: StreamflatMap can be used to transform an Optional into a Stream, allowing for further operations on the contained value.
---

**Contents**

[TOC]

# Introduction
Java 8's Optional is a container object which may or may not contain a non-null value. It provides a way to represent optional values instead of using null references. Stream::flatMap is used to transform each element of a stream into zero or more elements.

# How to Use Optional with Stream::flatMap
Optional can be used with Stream::flatMap in order to provide an efficient way to filter out non-existent values. It can also be used to transform a stream of Optional values into a stream of non-optional values.

# Example
Let's say we have a list of Optional<String> values and we want to filter out the non-existent values and transform the existing values into a list of non-optional Strings. We can use Stream::flatMap in combination with Optional to achieve this:

```
List<Optional<String>> optionalList = ...;
List<String> stringList = optionalList.stream()
                                     .flatMap(Optional::stream)
                                     .collect(Collectors.toList());
```

# Conclusion
Using Optional with Stream::flatMap is an efficient way to filter out non-existent values and transform a stream of Optional values into a stream of non-optional values. It can be used to simplify code and make it more readable.
