---
title: What is the best way to take out a portion of a given string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the String class`s replace() method to remove a substring from a given String in Java.
---

**Contents**

[TOC]

**Section 1: Substring Manipulation**

The most basic way to remove a substring from a given String in Java is to use the `String.replace()` method. This method takes two parameters: the substring to be replaced and the replacement string. The `replace()` method will replace all occurrences of the substring with the replacement string. For example:

```java
String str = "Hello World";
String newStr = str.replace("World", "");
// newStr is now "Hello "
```

**Section 2: Regular Expressions**

A more powerful approach to removing a substring from a given String is to use regular expressions. Regular expressions are a powerful tool for matching patterns in text and can be used to remove specific substrings from a given String. For example, the following code uses a regular expression to remove all digits from a given String:

```java
String str = "Hello 123 World";
String newStr = str.replaceAll("\\d", "");
// newStr is now "Hello  World"
```

**Section 3: StringBuilder**

Another approach to removing a substring from a given String is to use the `StringBuilder` class. The `StringBuilder` class provides methods for manipulating strings in a more efficient way than the `String` class. For example, the following code uses the `StringBuilder` class to remove a substring from a given String:

```java
String str = "Hello World";
StringBuilder sb = new StringBuilder(str);
int startIndex = str.indexOf("World");
int endIndex = startIndex + "World".length();
sb.delete(startIndex, endIndex);
String newStr = sb.toString();
// newStr is now "Hello "
```

**Section 4: Splitting**

Finally, a fourth approach to removing a substring from a given String is to use the `String.split()` method. This method takes a regular expression as its parameter and splits the String into an array of substrings based on the expression. The following code uses the `split()` method to remove a substring from a given String:

```java
String str = "Hello World";
String[] parts = str.split("World");
String newStr = parts[0];
// newStr is now "Hello "
```
