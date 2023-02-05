---
title: What is the procedure for determining if a particular character is present in a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the String.contains() method to check if a single character appears in a string in Java.
---

**Contents**

[TOC]

### Using the contains() Method

The `String` class in Java provides a `contains()` method which can be used to check if a `String` contains a particular character or a sequence of characters. The `contains()` method takes a `CharSequence` as an argument and returns a boolean value. 

```java
String str = "Hello World";

boolean containsChar = str.contains("W");

// returns true
```

### Using the indexOf() Method

The `String` class also provides an `indexOf()` method which can be used to check if a `String` contains a particular character. The `indexOf()` method takes a `char` value as an argument and returns the index of the first occurrence of the character in the `String`. If the character does not appear in the `String`, the `indexOf()` method returns `-1`.

```java
String str = "Hello World";

int index = str.indexOf('W');

// returns 6
```

### Using Regular Expressions

Regular expressions can also be used to check if a `String` contains a particular character. The `matches()` method of the `String` class can be used to check if a `String` matches a particular regular expression.

```java
String str = "Hello World";

boolean containsChar = str.matches(".*W.*");

// returns true
```

### Using the for Loop

Another way to check if a `String` contains a particular character is to loop through the `String` and check each character one by one.

```java
String str = "Hello World";
boolean containsChar = false;

for (int i = 0; i < str.length(); i++) {
  if (str.charAt(i) == 'W') {
    containsChar = true;
    break;
  }
}

// returns true
```
