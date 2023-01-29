---
title: Determining if a string is empty or null in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A string can be checked for emptiness or nullity in Java by using the String.isEmpty() or String.isBlank() methods.
---

**Contents**

[TOC]

### Solution 1: Using `String.isEmpty()`

The `String.isEmpty()` method can be used to check if a string is empty or null in Java. It returns `true` if the string is empty or `null`.

```java
String str = "";
if(str.isEmpty()) {
    System.out.println("String is empty or null");
}
```

### Solution 2: Comparing with `null`

The `null` keyword can be used to check if a string is empty or null in Java. It returns `true` if the string is empty or `null`.

```java
String str = "";
if(str == null) {
    System.out.println("String is empty or null");
}
```
