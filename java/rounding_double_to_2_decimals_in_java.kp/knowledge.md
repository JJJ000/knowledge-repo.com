---
title: Round to two decimal places
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DecimalFormat class to format the double to 2 decimal places.
---

**Contents**

[TOC]

### Math.round()

The `Math.round()` method can be used to round a double to 2 decimal places in Java.

### Syntax

The syntax for `Math.round()` is as follows:

```java
Math.round(doubleValue * 100.0) / 100.0;
```

### Example

To round a double to 2 decimal places in Java, the following example can be used:

```java
double value = 3.14159;
double roundedValue = Math.round(value * 100.0) / 100.0;
System.out.println(roundedValue); // Outputs 3.14
```

### Output

The output of the code above will be:

`3.14`
