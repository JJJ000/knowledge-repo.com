---
title: Transforming a list of objects into a string generated from the tostring method by utilizing streams
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the map() method on the Stream to call the toString() method on each object in the list, then use the collect() method to join the results into a single string.
---

**Contents**

[TOC]

### Section 1: Creating the Stream

First, create a Stream of the list of objects by using the `stream()` method on the list.

```java
List<Object> list = ...;
Stream<Object> stream = list.stream();
```

### Section 2: Using the Map Method

Next, use the `map()` method to map each object in the stream to its `toString()` representation.

```java
Stream<String> stringStream = stream.map(Object::toString);
```

### Section 3: Collecting the Stream

Finally, collect the stream into a String using the `collect()` method.

```java
String result = stringStream.collect(Collectors.joining());
```

### Section 4: Result

The resulting String will contain the `toString()` representations of each object in the list, concatenated together.
