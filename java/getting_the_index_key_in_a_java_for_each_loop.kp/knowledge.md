---
title: What is the syntax for obtaining the current index/key in a "for each" loop in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `forEach()` method to access the current index/key in a `for each` loop.
---

**Contents**

[TOC]

### Solution 1 - Using `for` Loop

When using a `for` loop, you can use the loop index to get the current index/key in the loop. For example:

```java
for (int i = 0; i < array.length; i++) {
    System.out.println("Current index/key: " + i);
    // do something with array[i]
}
```

### Solution 2 - Using `forEach` Method

When using the `forEach` method, you can use the `forEach` method's parameter to get the current index/key. For example:

```java
array.forEach((key, value) -> {
    System.out.println("Current index/key: " + key);
    // do something with value
});
```

### Solution 3 - Using `forEachRemaining` Method

When using the `forEachRemaining` method, you can use the `forEachRemaining` method's parameter to get the current index/key. For example:

```java
Iterator<Integer> iterator = array.iterator();
iterator.forEachRemaining(key -> {
    System.out.println("Current index/key: " + key);
    // do something with array[key]
});
```

### Solution 4 - Using `entrySet` Method

When using the `entrySet` method, you can use the `entrySet` method's parameter to get the current index/key. For example:

```java
Map<Integer, String> map = new HashMap<>();
map.entrySet().forEach(entry -> {
    System.out.println("Current index/key: " + entry.getKey());
    // do something with entry.getValue()
});
```
