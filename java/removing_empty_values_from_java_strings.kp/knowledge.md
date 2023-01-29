---
title: Empty values are excluded when using the Java string split method
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, Java`s String.split() method removes empty values.
---

**Contents**

[TOC]

### Definition
The `String.split()` method is used to split a string into an array of substrings, and returns the new array. 

### Functionality
The `String.split()` method takes a regular expression as a parameter, and will use it to determine where to split the string. By default, the `String.split()` method will remove any empty values from the resulting array. 

### Examples
For example, consider the following string:
```java
String str = "This,is,a,test,string";
```
Using the `String.split()` method with the default parameter, the resulting array would not contain any empty values:
```java
String[] arr = str.split(",");
// arr = ["This", "is", "a", "test", "string"]
```

### Conclusion
In conclusion, the `String.split()` method will remove any empty values from the resulting array by default. This behavior can be changed by providing a different regular expression as a parameter to the `String.split()` method.
