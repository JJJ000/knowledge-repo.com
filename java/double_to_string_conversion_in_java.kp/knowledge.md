---
title: Changing a double to a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Double class provides a toString() method which can be used to convert a double to a String.
---

**Contents**

[TOC]

#### Using toString()

The `toString()` method can be used to convert a double to a String. This method is defined in the `Double` class and accepts a double value as an argument. The following example illustrates how to use this method:

```java
double d = 10.5;
String s = Double.toString(d);
```

#### Using String.valueOf()

The `String.valueOf()` method can also be used to convert a double to a String. This method is defined in the `String` class and accepts a double value as an argument. The following example illustrates how to use this method:

```java
double d = 10.5;
String s = String.valueOf(d);
```

#### Using DecimalFormat

The `DecimalFormat` class can be used to convert a double to a String with a specific format. This class is defined in the `java.text` package and accepts a pattern as an argument. The following example illustrates how to use this class:

```java
double d = 10.5;
DecimalFormat df = new DecimalFormat("#.##");
String s = df.format(d);
```

#### Using StringBuffer

The `StringBuffer` class can also be used to convert a double to a String. This class is defined in the `java.lang` package and accepts a double value as an argument. The following example illustrates how to use this class:

```java
double d = 10.5;
StringBuffer sb = new StringBuffer();
sb.append(d);
String s = sb.toString();
```
