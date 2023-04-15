---
title: Verify that a string is not null or empty
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A String can be checked for not being null and not empty by using the method `String.isEmpty()` to check if the String is empty and `String != null` to check if the String is not null.
---

**Contents**

[TOC]

### Solution 1

### Using the `length()` method

Java provides a `length()` method for strings that returns the length of the string. If the length is greater than 0, then the string is not null and not empty.

```java
String str = "Hello World!";
if (str.length() > 0) {
    System.out.println("String is not null and not empty");
} else {
    System.out.println("String is either null or empty");
}
```

### Solution 2

### Using the `isEmpty()` method

Java provides an `isEmpty()` method for strings that returns true if the length of the string is 0. If the method returns false, then the string is not null and not empty.

```java
String str = "Hello World!";
if (!str.isEmpty()) {
    System.out.println("String is not null and not empty");
} else {
    System.out.println("String is either null or empty");
}
```
