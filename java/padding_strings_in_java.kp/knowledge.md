---
title: What is the best way to add extra characters to a string in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.format() method with `%s` as the first argument and the desired padding as the second argument.
---

**Contents**

[TOC]

### Using the StringUtils.leftPad Method

The `StringUtils.leftPad` method from the Apache Commons Lang library can be used to pad a String with a specified character.

Example:

```java
String str = "Hello";
String paddedStr = StringUtils.leftPad(str, 10, '*');

// paddedStr is now "****Hello"
```

### Using the String.format Method

The `String.format` method can be used to format a String with a specified character.

Example:

```java
String str = "Hello";
String paddedStr = String.format("%10s", str).replace(' ', '*');

// paddedStr is now "****Hello"
```

### Using the StringBuilder

The `StringBuilder` class can be used to manually pad a String with a specified character.

Example:

```java
String str = "Hello";
StringBuilder sb = new StringBuilder();
for (int i = 0; i < 10 - str.length(); i++) {
    sb.append('*');
}
sb.append(str);
String paddedStr = sb.toString();

// paddedStr is now "****Hello"
```

### Using the String.repeat Method (Java 11+)

The `String.repeat` method can be used to pad a String with a specified character.

Example:

```java
String str = "Hello";
String paddedStr = "*".repeat(10 - str.length()) + str;

// paddedStr is now "****Hello"
```
