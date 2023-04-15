---
title: What is the process of changing a long data type to a string data type?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Long.toString(long) method to convert a long to a String.
---

**Contents**

[TOC]

### Method 1: Using String.valueOf()
String.valueOf() is a static method that returns the string representation of the argument passed to it.

Syntax:
```
public static String valueOf(long l)
```

Example:
```
long longValue = 123456789;
String strValue = String.valueOf(longValue);
```

### Method 2: Using Long.toString()
Long.toString() is an instance method that returns the string representation of the long argument passed to it.

Syntax:
```
public String toString(long l)
```

Example:
```
long longValue = 123456789;
String strValue = Long.toString(longValue);
```

### Method 3: Using Long.toString(long, int)
Long.toString(long, int) is an instance method that returns the string representation of the long argument passed to it in the specified radix.

Syntax:
```
public String toString(long l, int radix)
```

Example:
```
long longValue = 123456789;
String strValue = Long.toString(longValue, 16);
```

### Method 4: Using DecimalFormat
DecimalFormat is a class that formats decimal numbers into strings.

Syntax:
```
public String format(long l)
```

Example:
```
long longValue = 123456789;
DecimalFormat df = new DecimalFormat("#");
String strValue = df.format(longValue);
```
