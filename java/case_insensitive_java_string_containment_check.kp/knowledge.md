---
title: What is the best way to determine if a string includes another string in a case insensitive manner in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String method contains() with the argument String.CASE\_INSENSITIVE\_ORDER.
---

**Contents**

[TOC]

### Using `String.contains()`

The `String.contains()` method can be used to check if a String contains another String in a case insensitive manner. This method returns a `boolean` value of `true` if the specified String is found in the given String, and `false` otherwise.

```java
String str1 = "Hello World";
String str2 = "hello";

boolean contains = str1.contains(str2); // contains = true
```

### Using `String.toLowerCase()`

The `String.toLowerCase()` method can be used to convert both the Strings to lowercase before comparing them. This method returns a new String object with all the characters of the String converted to lowercase.

```java
String str1 = "Hello World";
String str2 = "hello";

boolean contains = str1.toLowerCase().contains(str2.toLowerCase()); // contains = true
```

### Using `String.equalsIgnoreCase()`

The `String.equalsIgnoreCase()` method can also be used to check if a String contains another String in a case insensitive manner. This method returns a `boolean` value of `true` if the specified String is found in the given String, and `false` otherwise.

```java
String str1 = "Hello World";
String str2 = "hello";

boolean contains = str1.equalsIgnoreCase(str2); // contains = true
```

### Using `StringUtils.containsIgnoreCase()`

The `StringUtils.containsIgnoreCase()` method from the Apache Commons Lang library can also be used to check if a String contains another String in a case insensitive manner. This method returns a `boolean` value of `true` if the specified String is found in the given String, and `false` otherwise.

```java
String str1 = "Hello World";
String str2 = "hello";

boolean contains = StringUtils.containsIgnoreCase(str1, str2); // contains = true
```
