---
title: What is the best way to divide a string using any type of whitespace character as a separator?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the split() method of the String class, passing a regular expression that matches any whitespace characters as the delimiter.
---

**Contents**

[TOC]

1. **Using the `split()` Method**

The `split()` method can be used to split a String object into an array of substrings by using a given delimiter.

2. **Syntax**

The syntax for the `split()` method is as follows:

`String.split(String regex)`

Where `regex` is the delimiter used to separate the substrings.

3. **Example**

The following example shows how to split a String object using a whitespace character as the delimiter:

```java
String str = "This is a test string";
String[] arr = str.split("\\s+");
```

The `arr` array will contain the following substrings:

`["This", "is", "a", "test", "string"]`

4. **Note**

Note that the `split()` method takes a regular expression as its argument, so if you want to use any whitespace character as the delimiter, you should use the `\\s+` regex.
