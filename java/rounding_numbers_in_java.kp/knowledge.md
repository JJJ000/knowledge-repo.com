---
title: What is the syntax for rounding a number to n decimal places in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String.format() method with the format specifier `%.nf` to round a number to n decimal places in Java.
---

**Contents**

[TOC]

### Solution

### Using Math.round()

The Math.round() method can be used to round a number to a specified number of decimal places. The syntax for this method is as follows:

`Math.round(double number * 10^n) / 10^n`

Where `number` is the number to be rounded and `n` is the number of decimal places to round to.

For example, to round the number 3.14159 to two decimal places, the expression `Math.round(3.14159 * 10^2) / 10^2` would be used. This expression evaluates to 3.14.

### Using DecimalFormat

The DecimalFormat class can also be used to round a number to a specified number of decimal places. The syntax for this class is as follows:

`DecimalFormat df = new DecimalFormat("#.##");`

Where the number of decimal places is specified by the number of hash symbols (#) after the decimal point.

For example, to round the number 3.14159 to two decimal places, the expression `DecimalFormat df = new DecimalFormat("#.##");` would be used. This expression evaluates to 3.14.
