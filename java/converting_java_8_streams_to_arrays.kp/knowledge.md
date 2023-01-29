---
title: What is the process for transforming a Java 8 stream into an array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Stream.toArray() method.
---

**Contents**

[TOC]

### Create a Stream

The first step in converting a Java 8 Stream to an Array is to create a Stream. This can be done using the `Stream.of()` method. This method takes in a variable number of arguments and returns a Stream containing the arguments.

For example,

```java
Stream<String> stream = Stream.of("foo", "bar", "baz");
```

### Convert Stream to Array

Once a Stream has been created, it can be converted to an Array using the `toArray()` method. This method takes in a `IntFunction` as an argument and returns an array of the type specified by the `IntFunction`.

For example,

```java
String[] array = stream.toArray(String[]::new);
```

### Check Array

Once the Stream has been converted to an Array, it is important to check the Array to make sure that it contains the expected elements. This can be done using the `assertArrayEquals()` method.

For example,

```java
assertArrayEquals(new String[]{"foo", "bar", "baz"}, array);
```

### Use Array

Finally, the Array can be used for whatever purpose is desired. For example, the Array can be iterated over to print out each element, or it can be used as an argument for a method. 

For example,

```java
for (String s : array) {
    System.out.println(s);
}
```
