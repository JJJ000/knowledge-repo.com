---
title: What method can be used to determine if a double is equal to nan?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can test if a double is equal to NaN by using the Double.isNaN(double) method.
---

**Contents**

[TOC]

### Using isNaN()
The isNaN() method is used to check if a double is equal to NaN. This method returns a boolean value, true if the double is equal to NaN and false if it is not.

Syntax:
```
public static boolean isNaN(double d)
```

Example:
```
double d1 = Double.NaN;
System.out.println(Double.isNaN(d1)); // Outputs true

double d2 = 0.0;
System.out.println(Double.isNaN(d2)); // Outputs false
```

### Using == Operator
The == operator can also be used to check if a double is equal to NaN. However, it is not recommended to use this method as it can lead to unexpected results.

Syntax:
```
double d == Double.NaN
```

Example:
```
double d1 = Double.NaN;
System.out.println(d1 == Double.NaN); // Outputs false

double d2 = 0.0;
System.out.println(d2 == Double.NaN); // Outputs false
```
