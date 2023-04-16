---
title: What is the best way to compare two integers in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Integer.compare() method.
---

**Contents**

[TOC]

#Comparing Integers with '=='
The most straightforward way to compare two integers is to use the '==' operator. This operator checks to see if two values are equal. If the two values are equal, the expression evaluates to true.

#Comparing Integers with 'compareTo()'
The 'compareTo()' method is another way to compare two integers. This method returns an integer value that is a result of the comparison. If the two values are equal, the result is 0. If the first value is greater than the second, the result is a positive integer. If the first value is less than the second, the result is a negative integer.

#Comparing Integers with 'equals()'
The 'equals()' method is another way to compare two integers. This method returns a boolean value that is the result of the comparison. If the two values are equal, the result is true. If the two values are not equal, the result is false.

#Comparing Integers with 'compare()'
The 'compare()' method is a static method in the Integer class that is used to compare two integers. This method returns an integer value that is a result of the comparison. If the two values are equal, the result is 0. If the first value is greater than the second, the result is a positive integer. If the first value is less than the second, the result is a negative integer.
