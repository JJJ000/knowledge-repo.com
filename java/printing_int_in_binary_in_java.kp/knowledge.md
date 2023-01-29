---
title: Output an integer in binary form using java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Integer.toBinaryString(int) method to print an integer in binary format in Java.
---

**Contents**

[TOC]

### Method 1

Using the `Integer.toBinaryString()` method:

```java
int x = 10;
String binaryString = Integer.toBinaryString(x);
System.out.println(binaryString);
```

### Output

`1010`

### Method 2

Using the `Integer.toString()` method with a radix of 2:

```java
int x = 10;
String binaryString = Integer.toString(x, 2);
System.out.println(binaryString);
```

### Output

`1010`
