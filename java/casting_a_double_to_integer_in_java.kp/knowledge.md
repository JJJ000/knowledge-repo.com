---
title: Convert a double to an integer in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The double value can be cast to an integer by using the (int) operator.
---

**Contents**

[TOC]

### Using Casting

Casting is the process of converting one data type to another. In Java, we can cast a double to an integer by using the (int) prefix. The syntax for this is as follows:

```
int myInteger = (int) myDouble;
```

This will convert the double value stored in the variable myDouble to an integer value stored in the variable myInteger.

### Using Math.round()

Another way to cast a double to an integer is to use the Math.round() method. This method will round the double value to the nearest integer. The syntax for this is as follows:

```
int myInteger = Math.round(myDouble);
```

### Using Math.floor()

The Math.floor() method can also be used to cast a double to an integer. This method will round the double value down to the nearest integer. The syntax for this is as follows:

```
int myInteger = (int) Math.floor(myDouble);
```

### Using Math.ceil()

The Math.ceil() method can also be used to cast a double to an integer. This method will round the double value up to the nearest integer. The syntax for this is as follows:

```
int myInteger = (int) Math.ceil(myDouble);
```
