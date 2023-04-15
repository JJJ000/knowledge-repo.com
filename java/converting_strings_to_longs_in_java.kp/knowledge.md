---
title: What is the process for changing a string to a long in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Long.parseLong() method to convert a String to a long in Java.
---

**Contents**

[TOC]

### Using the Long.parseLong() Method

The Long.parseLong() method is used to convert a String to a long in Java. This method takes a String as an argument and returns a long value.

### Example

Let's look at an example of how to use the Long.parseLong() method.

```java
String str = "12345";
long num = Long.parseLong(str);
System.out.println(num);
```

The output of this code would be:

```
12345
```

### Using the Long.valueOf() Method

The Long.valueOf() method is another way to convert a String to a long in Java. This method takes a String as an argument and returns a Long object.

### Example

Let's look at an example of how to use the Long.valueOf() method.

```java
String str = "12345";
Long num = Long.valueOf(str);
System.out.println(num);
```

The output of this code would be:

```
12345
```
