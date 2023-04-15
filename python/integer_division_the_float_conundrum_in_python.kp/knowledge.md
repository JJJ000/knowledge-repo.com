---
title: What is the reason for obtaining a float instead of another integer from integer division?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To maintain decimal precision and avoid losing information during the division process.
---

**Contents**

[TOC]

Section 1: Introduction 
Python is a high-level programming language which supports a wide range of data types. One of the basic data types is an integer. It is a whole number which can be positive, negative or zero. When we perform arithmetic operations on integers, sometimes we encounter a scenario where we expect the result to be an integer, but we get the value in the float data type. This happens when we perform division of two integers, and the result leads to a fractional value.

Section 2: Division in Python
Division is a fundamental arithmetic operation which is present in every programming language. Python provides two types of division operators: 

a. Integer division
b. Floating-point division

The integer division, represented by two forward slashes (//), performs the division operation between the two numbers and returns the quotient as an integer. The floating-point division, represented by a forward slash (/), performs division between the two numbers and returns the quotient as a floating-point number.

Section 3: Why integer division yields a float in Python?
When we perform integer division in Python and the quotient turns out to be a fractional value, then we get the result in float data type instead of integer. For instance, if we perform the division operation 15 // 4, the expected output is 3, but we get 3.75 (float value). So, why does that happen?
This is because when Python encounters the division operation, it first performs the division between the two integers and then checks whether the quotient has a fractional part or not. If it has a fractional part, then it returns the result in float data type to preserve the accuracy of the quotient and the remaining fractional value. Python emphasizes precision over integer conversion and hence yields a floating-point value by default.

Section 4: Conclusion
By default, integer division yields a float in Python if the quotient has a fractional part. This is because Python emphasizes the accuracy and precision of the calculation over integer conversion. Therefore, it is imperative to be aware of this behavior when dealing with integer division operations in Python.
