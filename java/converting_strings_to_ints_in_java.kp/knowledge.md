---
title: What is the process for changing a string to an int in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Use the `Integer.parseInt()` method to convert a String to an int in Java.
---

**Contents**

[TOC]

### Using Integer.parseInt()
The `Integer.parseInt()` method is the most common way to convert a string to an integer in Java. This method takes the string to be converted as its first parameter and returns the integer value represented by the string.

Syntax:
```java
int intValue = Integer.parseInt(stringValue);
```

Example:
```java
String str = "123";
int num = Integer.parseInt(str);
System.out.println(num); // Outputs 123
```

### Using Integer.valueOf()
The `Integer.valueOf()` method is another way to convert a string to an integer in Java. This method takes the string to be converted as its first parameter and returns an `Integer` object.

Syntax:
```java
Integer intObject = Integer.valueOf(stringValue);
```

Example:
```java
String str = "123";
Integer num = Integer.valueOf(str);
System.out.println(num); // Outputs 123
```

### Using DecimalFormat
The `DecimalFormat` class can also be used to convert a string to an integer in Java. This class takes the string to be converted as its first parameter and returns the integer value represented by the string.

Syntax:
```java
DecimalFormat df = new DecimalFormat();
int intValue = df.parse(stringValue).intValue();
```

Example:
```java
String str = "123";
DecimalFormat df = new DecimalFormat();
int num = df.parse(str).intValue();
System.out.println(num); // Outputs 123
```
