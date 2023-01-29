---
title: What is the best way to add zeros to the beginning of an integer?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String.format() method to format an integer with the desired padding of zeros.
---

**Contents**

[TOC]

### Option 1: Using String.format

The `String.format()` method can be used to pad a number with zeros on the left. The syntax is as follows:

```java
String.format("%0[number of zeros]d", [number])
```

For example, to pad the number `123` with three zeros on the left, use the following code:

```java
String result = String.format("%06d", 123);
```

The result will be `000123`.

### Option 2: Using StringBuilder

The `StringBuilder` class can be used to pad a number with zeros on the left. The syntax is as follows:

```java
StringBuilder sb = new StringBuilder();
sb.append(String.format("%0[number of zeros]d", [number]));
String result = sb.toString();
```

For example, to pad the number `123` with three zeros on the left, use the following code:

```java
StringBuilder sb = new StringBuilder();
sb.append(String.format("%06d", 123));
String result = sb.toString();
```

The result will be `000123`.

### Option 3: Using DecimalFormat

The `DecimalFormat` class can be used to pad a number with zeros on the left. The syntax is as follows:

```java
DecimalFormat df = new DecimalFormat("0[number of zeros]");
String result = df.format([number]);
```

For example, to pad the number `123` with three zeros on the left, use the following code:

```java
DecimalFormat df = new DecimalFormat("000");
String result = df.format(123);
```

The result will be `000123`.
