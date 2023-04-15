---
title: What are the differences between double and bigdecimal?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: BigDecimal is a more precise and accurate way to represent decimal numbers in Java, while Double is less precise but faster to compute.
---

**Contents**

[TOC]

### Double
Double is a primitive data type used to represent numbers with decimal points. It is the default data type for representing numbers in Java. It is a 64-bit IEEE 754 floating point value and can represent numbers from 1.7e−308 to 1.7e+308 with a precision of 15-16 digits.

### BigDecimal
BigDecimal is a wrapper class for arbitrary-precision signed decimal numbers. It is used for calculations that require a higher degree of accuracy than what is available with the primitive double type. It is a immutable class with arbitrary-precision signed decimal numbers that can represent numbers from -2^1024 to 2^1024 with a precision of up to 34 digits.

### Advantages of Double
- Double is faster than BigDecimal as it takes less time to process.
- Double is more memory efficient as it takes up less space than BigDecimal.

### Advantages of BigDecimal
- BigDecimal provides greater accuracy as it can represent numbers with a precision of up to 34 digits.
- BigDecimal is more suitable for financial calculations as it provides a higher degree of accuracy.
