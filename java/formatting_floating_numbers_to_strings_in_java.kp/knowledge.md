---
title: How to convert floating numbers to a string with appropriate formatting and no extra decimal places?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use String.format(`%.<number of decimal places>f`, <float number>) to format a float to a String with the desired precision.
---

**Contents**

[TOC]

1. Using `String.format()` 
  
  The `String.format()` method can be used to format a floating point number into a string representation. The `%f` flag is used to format a float or double value. The number of decimal places to be used can be specified by passing the number of decimal places as an argument to the `String.format()` method. 

2. Using `DecimalFormat` 

  The `DecimalFormat` class can be used to format floating point numbers into string representations. The `DecimalFormat` class provides a `setMinimumFractionDigits()` and `setMaximumFractionDigits()` methods which can be used to specify the number of decimal places to be used.

3. Using `NumberFormat` 

  The `NumberFormat` class can also be used to format floating point numbers into string representations. The `NumberFormat` class provides a `setMinimumFractionDigits()` and `setMaximumFractionDigits()` methods which can be used to specify the number of decimal places to be used.

4. Using `BigDecimal` 

  The `BigDecimal` class can be used to format floating point numbers into string representations. The `BigDecimal` class provides a `setScale()` method which can be used to specify the number of decimal places to be used. The `BigDecimal` class also provides a `stripTrailingZeros()` method which can be used to remove unnecessary trailing zeros.
