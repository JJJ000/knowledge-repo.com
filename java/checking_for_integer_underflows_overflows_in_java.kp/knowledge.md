---
title: What methods does Java use to prevent and detect integer underflows and overflows, and how can one verify this?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Java handles integer underflows and overflows by wrapping the value around to the opposite end of the range of values, and you can check for it by comparing the result to the expected value.
---

**Contents**

[TOC]

## Integer Underflows

When an integer underflows, the value of the integer is set to the lowest value that is representable in the integer data type. In Java, this value is -2,147,483,648 for a 32-bit integer.

## Integer Overflows

When an integer overflows, the value of the integer is set to the highest value that is representable in the integer data type. In Java, this value is 2,147,483,647 for a 32-bit integer.

## Checking for Integer Overflows/Underflows

One way to check for integer overflows/underflows is to use the Integer.MAX_VALUE and Integer.MIN_VALUE constants provided by the Java API. These constants represent the highest and lowest values that can be represented by a 32-bit integer. If a value is greater than Integer.MAX_VALUE or less than Integer.MIN_VALUE, then an overflow/underflow has occurred.

Another way to check for integer overflows/underflows is to use the Integer.compare() method. This method takes two integers as arguments and returns an integer value that indicates the comparison between the two integers. If the return value is greater than 0, then the first integer is greater than the second. If the return value is less than 0, then the first integer is less than the second. If the return value is 0, then the two integers are equal. This method can be used to check if an integer is greater than Integer.MAX_VALUE or less than Integer.MIN_VALUE, which would indicate an overflow/underflow.
