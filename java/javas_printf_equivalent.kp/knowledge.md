---
title: What is the Java equivalent of sprintf?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: In Java, the equivalent of sprintf is the String.format() method.
---

**Contents**

[TOC]

1. Using `String.format()` 
   
   `String.format()` is a static method in the `String` class that allows you to create a formatted string. It takes a format string and any number of objects as arguments. The format string can contain literal text and format specifiers, which are special characters that are replaced by the values of the arguments.

2. Using `StringBuilder` 
   
   `StringBuilder` is a class that provides a mutable sequence of characters. It can be used to create a formatted string by appending literal text and the `append()` method. The `append()` method takes an argument of type `Object` and calls its `toString()` method to convert it to a `String`.

3. Using `MessageFormat` 
   
   `MessageFormat` is a class in the `java.text` package that provides a way to create formatted strings by using a pattern string and an array of arguments. The pattern string can contain literal text and format elements, which are special characters that are replaced by the values of the arguments.

4. Using `Formatter` 
   
   `Formatter` is a class in the `java.util` package that provides a way to create formatted strings by using a format string and an array of arguments. The format string can contain literal text and format specifiers, which are special characters that are replaced by the values of the arguments.
