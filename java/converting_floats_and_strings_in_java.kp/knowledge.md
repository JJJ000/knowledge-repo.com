---
title: Change a float to a string and a string to a float in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Float can be converted to String using the Float.toString() method, and String can be converted to float using the Float.parseFloat() method.
---

**Contents**

[TOC]

#### Float to String

Converting a float to a String in Java can be done using the `String.valueOf(float)` method. The following example shows how to use this method:

```java
float f = 1.23f;
String s = String.valueOf(f);
System.out.println("String is: " + s);
```

#### String to Float

Converting a String to a float in Java can be done using the `Float.parseFloat(String)` method. The following example shows how to use this method:

```java
String s = "1.23";
float f = Float.parseFloat(s);
System.out.println("Float is: " + f);
```
