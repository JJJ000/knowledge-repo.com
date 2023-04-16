---
title: How do you format a number to two decimal places in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DecimalFormat class to round to two decimal places in Java.
---

**Contents**

[TOC]

# Math.round

Math.round() is a Java method that can be used to round a number to a specified number of decimal places.

## Syntax

The syntax for Math.round() is as follows: 

```
Math.round(double number * 10^decimalPlaces) / 10^decimalPlaces
```

## Example

To round a number to two decimal places, the syntax would be:

```
Math.round(double number * 100.0) / 100.0
```

## Usage

To round a number to two decimal places, the following code can be used:

```
double number = 2.5678;
double roundedNumber = Math.round(number * 100.0) / 100.0;
System.out.println(roundedNumber); // Outputs 2.57
```
