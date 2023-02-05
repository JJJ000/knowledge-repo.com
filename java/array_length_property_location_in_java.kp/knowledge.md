---
title: What is the source of the length property of an array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The length property of an array in Java is defined in the java.lang.reflect.Array class.
---

**Contents**

[TOC]

### Class Definition
The length property of an array is defined in the java.lang.reflect.Array class.

### Syntax
The syntax for accessing the length property of an array is as follows:
```
int length = array.length;
```

### Description
The length property of an array is an integer value that indicates the number of elements in the array. It is a read-only property and cannot be modified.

### Example
The following example shows how to access the length of an array:
```
int[] array = {1, 2, 3, 4};
int length = array.length;
System.out.println("Length of array: " + length);
```
The output of the above code will be:
```
Length of array: 4
```
