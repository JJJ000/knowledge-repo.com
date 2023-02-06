---
title: Round a float to n decimal places
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String.format() method with the %.<n>f format specifier to format a float to n decimal places in Java.
---

**Contents**

[TOC]

## Using DecimalFormat
The DecimalFormat class can be used to format a float to a specified number of decimal places.

Syntax: 

```java
DecimalFormat df = new DecimalFormat("#.####");
String str = df.format(floatNumber);
```

Example: 

```java
float floatNumber = 12.3456f;
DecimalFormat df = new DecimalFormat("#.####");
String str = df.format(floatNumber);
System.out.println(str);
```

Output: 

```
12.3456
```

## Using String.format
The String.format() method can also be used to format a float to a specified number of decimal places.

Syntax: 

```java
String str = String.format("%.nf", floatNumber);
```

Example: 

```java
float floatNumber = 12.3456f;
String str = String.format("%.2f", floatNumber);
System.out.println(str);
```

Output: 

```
12.35
```
