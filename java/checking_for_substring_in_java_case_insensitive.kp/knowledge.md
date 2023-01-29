---
title: What is the syntax for determining if a substring exists in a string (ignoring case) in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String.contains() method with the ignoreCase parameter set to true.
---

**Contents**

[TOC]

**1. Using the `contains()` Method**

The `contains()` method is a method of the `String` class that returns a boolean indicating whether or not a given string contains a specified substring. This method is case-sensitive, meaning that it will only return `true` if the exact substring is found.

```java
String str = "Hello World";
boolean containsSubstring = str.contains("world"); // returns false
```

**2. Using the `indexOf()` Method**

The `indexOf()` method is another method of the `String` class that returns the index of the first occurrence of a specified substring within a given string. This method is also case-sensitive and will return `-1` if the substring is not found.

```java
String str = "Hello World";
int index = str.indexOf("world"); // returns -1
```

**3. Using the `toLowerCase()` Method**

The `toLowerCase()` method is a method of the `String` class that returns a new string with all characters converted to lowercase. This method can be used in conjunction with the `contains()` or `indexOf()` methods to ignore the case of the substring.

```java
String str = "Hello World";
boolean containsSubstring = str.toLowerCase().contains("world"); // returns true
```

**4. Using the `equalsIgnoreCase()` Method**

The `equalsIgnoreCase()` method is a method of the `String` class that returns a boolean indicating whether or not two strings are equal when ignoring case. This method can be used to check if a string contains a substring, as long as the substring is only one character.

```java
String str = "Hello World";
boolean containsSubstring = str.equalsIgnoreCase("h"); // returns true
```
