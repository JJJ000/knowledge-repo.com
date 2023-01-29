---
title: Change a string to a double in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Double.parseDouble(String) can be used to convert a String to a double in Java.
---

**Contents**

[TOC]

### Using the Double.parseDouble() Method

The Double.parseDouble() method is a static method belonging to the Double class. It is used to convert a String containing a numerical value into a double primitive.

Syntax:
```
public static double parseDouble(String s)
```

Example:
```
String str = "3.14";
double d = Double.parseDouble(str);
```

### Using the Double.valueOf() Method

The Double.valueOf() method is a static method belonging to the Double class. It is used to convert a String containing a numerical value into a Double object.

Syntax:
```
public static Double valueOf(String s)
```

Example:
```
String str = "3.14";
Double d = Double.valueOf(str);
```

### Using the DecimalFormat Class

The DecimalFormat class is used to format a numerical value as a String. It can then be converted to a double using the Double.parseDouble() method.

Syntax:
```
DecimalFormat df = new DecimalFormat("#.##");
double d = Double.parseDouble(df.format(3.14));
```

### Using the NumberFormat Class

The NumberFormat class is used to parse a String containing a numerical value into a double.

Syntax:
```
NumberFormat nf = NumberFormat.getInstance();
double d = nf.parse("3.14").doubleValue();
```
