---
title: What is the syntax for printing a float with two decimal places in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use String.format(`%.2f`, floatValue) to print a float with 2 decimal places in Java.
---

**Contents**

[TOC]

## Using `String.format()`
The simplest way to print a float with two decimal places is to use the `String.format()` method.

```java
float f = 3.14159;
System.out.println(String.format("%.2f", f));
```

## Using `DecimalFormat`
Another way to print a float with two decimal places is to use the `DecimalFormat` class.

```java
float f = 3.14159;
DecimalFormat df = new DecimalFormat("#.##");
System.out.println(df.format(f));
```

## Using `printf`
It is also possible to use the `printf` method to print a float with two decimal places.

```java
float f = 3.14159;
System.out.printf("%.2f", f);
```

## Using `BigDecimal`
Finally, it is possible to use the `BigDecimal` class to print a float with two decimal places.

```java
float f = 3.14159;
BigDecimal bd = new BigDecimal(f);
bd = bd.setScale(2, RoundingMode.HALF_UP);
System.out.println(bd);
```
