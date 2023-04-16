---
title: What is the method for extracting the file name from a string containing an absolute file path?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Path class` getFileName() method.
---

**Contents**

[TOC]

1. **Using substring() Method**

The `substring()` method of the `String` class can be used to get the file name from an absolute file path. This method takes two parameters, the start index and the end index. The start index is the index of the first character of the file name and the end index is the index of the last character of the file name.

2. **Using split() Method**

The `split()` method of the `String` class can also be used to get the file name from an absolute file path. This method takes a regular expression as a parameter and returns an array of strings. The last element of the array will be the file name.

3. **Using lastIndexOf() Method**

The `lastIndexOf()` method of the `String` class can be used to get the start index of the file name. This method takes a character as a parameter and returns the index of the last occurrence of the character in the string. The file name can then be obtained using the `substring()` method.

4. **Using Path Class**

The `Path` class in the `java.nio` package can also be used to get the file name from an absolute file path. This class has a method called `getFileName()` which returns the file name as a `Path` object. The `toString()` method of the `Path` object can be used to get the file name as a `String`.
