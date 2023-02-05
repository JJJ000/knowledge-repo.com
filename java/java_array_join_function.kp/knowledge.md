---
title: What is the Java equivalent of php's join() function for arrays?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Java equivalent of PHP`s join() function is the String.join() method.
---

**Contents**

[TOC]

### String.join()
The `String.join()` method in Java can be used to join elements of an array into a single string. It takes two arguments: a delimiter and an array of strings. The delimiter is used to separate the elements of the array, and the array is used to specify the elements that are to be joined. 

### Syntax
The syntax of the `String.join()` method is as follows:
```
String.join(delimiter, array);
```

### Example
For example, if we have an array of strings as follows:
```
String[] array = {"Hello", "World"};
```

We can join the elements of the array using the `String.join()` method as follows:
```
String joinedString = String.join(" ", array);
```

The `joinedString` variable will now contain the string `"Hello World"`.
