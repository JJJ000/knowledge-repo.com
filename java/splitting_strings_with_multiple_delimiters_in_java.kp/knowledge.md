---
title: Split a string using multiple delimiters with string.split()
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, String.split() can be used with multiple delimiters in Java by passing a regular expression as an argument.
---

**Contents**

[TOC]

### 1. Definition
String.split() is a Java method that splits a string into an array of substrings based on a given delimiter. It takes a single parameter, the delimiter, which is a character or a string that separates the substrings. 

### 2. Multiple Delimiters
String.split() can be used with multiple delimiters. To do this, the delimiters must be specified in a regular expression. A regular expression is a sequence of characters that define a search pattern. 

### 3. Example
For example, the following code uses the String.split() method to split a string into an array of substrings using multiple delimiters:

```java
String str = "apple,banana;cherry.orange";
String[] substrings = str.split("[,;.]");
```

In this example, the delimiters are a comma (`,`), a semicolon (`;`), and a period (`.`). The regular expression `[,;.]` specifies these delimiters.

### 4. Output
The output of this code is an array of four strings: `["apple", "banana", "cherry", "orange"]`.
