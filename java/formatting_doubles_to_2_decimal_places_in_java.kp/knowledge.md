---
title: How to most effectively round a double to two decimal places
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The best way to format a double value to 2 decimal places in Java is to use the DecimalFormat class and set the format to `0.00`.
---

**Contents**

[TOC]

### Using DecimalFormat

The DecimalFormat class can be used to format a double value to two decimal places.

```java
DecimalFormat df = new DecimalFormat("#.##");
double value = 12.34567;
String output = df.format(value);
System.out.println(output);
```

The output will be `12.35`.

### Using String.format

The String.format method can also be used to format a double value to two decimal places.

```java
double value = 12.34567;
String output = String.format("%.2f", value);
System.out.println(output);
```

The output will be `12.35`.

### Using NumberFormat

The NumberFormat class can be used to format a double value to two decimal places.

```java
NumberFormat nf = NumberFormat.getInstance();
nf.setMaximumFractionDigits(2);
double value = 12.34567;
String output = nf.format(value);
System.out.println(output);
```

The output will be `12.35`.

### Using Math.round

The Math.round method can be used to round a double value to two decimal places.

```java
double value = 12.34567;
double output = Math.round(value*100.0)/100.0;
System.out.println(output);
```

The output will be `12.35`.
