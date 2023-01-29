---
title: What is the process for adding together a list of integers using Java streams?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the IntStream.sum() method to sum a list of integers with Java streams.
---

**Contents**

[TOC]

### 1. Create a Stream

The first step is to create a Stream from the list of integers. This can be done using the `Stream.of()` method, which takes a variable number of arguments.

```java
List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);
Stream<Integer> stream = Stream.of(list);
```

### 2. Perform the Sum

Once the Stream has been created, the `sum()` method can be used to sum the elements of the Stream.

```java
int sum = stream.sum();
```

### 3. Print the Result

The result of the sum can be printed using the `System.out.println()` method.

```java
System.out.println("The sum of the list is " + sum);
```

### 4. Close the Stream

Finally, the Stream should be closed using the `close()` method.

```java
stream.close();
```
