---
title: What is the process for converting an array to a set in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To convert an Array to a Set in Java, use the constructor of the Set class that takes an Array as an argument.
---

**Contents**

[TOC]

### 1. Create a Set

To convert an Array to a Set in Java, the first step is to create a Set. This can be done by instantiating an implementation of the Set interface. For example, a `HashSet` can be created as follows:

```java
Set<String> set = new HashSet<>();
```

### 2. Add Array Elements to Set

Once the Set has been created, the elements of the Array can be added to the Set one by one. The `add()` method can be used to add a single element to the Set. For example, if the Array contains the elements `"a"`, `"b"`, and `"c"`, they can be added to the Set as follows:

```java
set.add("a");
set.add("b");
set.add("c");
```

### 3. Use Streams

Alternatively, Java 8 Streams can be used to add all the elements of the Array to the Set in one step. The `Stream.of()` method can be used to create a Stream from the Array, and the `forEach()` method can be used to add each element to the Set. For example, if the Array contains the elements `"a"`, `"b"`, and `"c"`, they can be added to the Set as follows:

```java
Stream.of("a", "b", "c").forEach(set::add);
```

### 4. Use Collection Utility

Finally, the `addAll()` method of the `Collections` utility class can be used to add all the elements of the Array to the Set in one step. For example, if the Array contains the elements `"a"`, `"b"`, and `"c"`, they can be added to the Set as follows:

```java
Collections.addAll(set, "a", "b", "c");
```
