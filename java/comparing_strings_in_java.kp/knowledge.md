---
title: What is the process for comparing strings in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To compare strings in Java, use the String.equals() or String.equalsIgnoreCase() methods.
---

**Contents**

[TOC]

### Using the equals() Method
The `equals()` method can be used to compare two strings for equality. This method returns `true` if the two strings are equal, and `false` otherwise. 

```java
String str1 = "Hello";
String str2 = "Hello";

boolean result = str1.equals(str2);
System.out.println(result); // prints true
```

### Using the compareTo() Method
The `compareTo()` method can be used to compare two strings lexicographically. This method returns an `int` value which is:
* Less than 0 if the first string is lexicographically less than the second
* Greater than 0 if the first string is lexicographically greater than the second
* Equal to 0 if the two strings are lexicographically equal

```java
String str1 = "Hello";
String str2 = "World";

int result = str1.compareTo(str2);
System.out.println(result); // prints -15
```

### Using the equalsIgnoreCase() Method
The `equalsIgnoreCase()` method can be used to compare two strings for equality, ignoring the case of the strings. This method returns `true` if the two strings are equal, ignoring the case, and `false` otherwise. 

```java
String str1 = "Hello";
String str2 = "HELLO";

boolean result = str1.equalsIgnoreCase(str2);
System.out.println(result); // prints true
```

### Using the compareToIgnoreCase() Method
The `compareToIgnoreCase()` method can be used to compare two strings lexicographically, ignoring the case of the strings. This method returns an `int` value which is:
* Less than 0 if the first string is lexicographically less than the second, ignoring the case
* Greater than 0 if the first string is lexicographically greater than the second, ignoring the case
* Equal to 0 if the two strings are lexicographically equal, ignoring the case

```java
String str1 = "Hello";
String str2 = "HELLO";

int result = str1.compareToIgnoreCase(str2);
System.out.println(result); // prints 0
```
