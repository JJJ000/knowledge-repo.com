---
title: Divide a string on an Android device
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String.split() method to split a string in Java.
---

**Contents**

[TOC]

# Section 1: String.split()
The simplest way to split a string in Java is to use the `String.split()` method. This method takes a string as an argument and returns a `String[]` array containing the substrings that were delimited by the argument.

# Section 2: Regular Expressions
The `String.split()` method can also accept a regular expression as an argument. This allows for more complex string splitting operations, such as splitting a string based on multiple delimiters or splitting a string based on a pattern.

# Section 3: StringTokenizer
The `StringTokenizer` class can also be used to split a string. This class takes a string as an argument and returns a `StringTokenizer` object, which can be iterated over to get the individual tokens.

# Section 4: Manual Splitting
Finally, it is also possible to manually split a string by looping over the characters of the string and checking for the desired delimiters. This method is not recommended as it is more time-consuming and error-prone than the other methods outlined above.
