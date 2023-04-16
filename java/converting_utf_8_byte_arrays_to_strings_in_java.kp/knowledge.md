---
title: Convert a utf-8 byte array to a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String constructor that takes a byte array and an encoding type, such as `UTF-8`, as parameters to convert a UTF-8 byte array to a String.
---

**Contents**

[TOC]

## String Constructor

The simplest way to convert a byte array to a String is to use the String constructor that accepts a byte array as an argument.

```java
String str = new String(byteArray);
```

## String.valueOf() Method

The String.valueOf() method is also used to convert a byte array to a String. It takes a byte array as an argument and returns a String representation of the byte array.

```java
String str = String.valueOf(byteArray);
```

## StringBuilder

The StringBuilder class can also be used to convert a byte array to a String. The StringBuilder class provides a mutable sequence of characters and has a constructor that accepts a byte array.

```java
StringBuilder sb = new StringBuilder(byteArray);
String str = sb.toString();
```

## Charset

The Charset class can be used to convert a byte array to a String. The Charset class provides a static method, named "forName()", which takes a character encoding name as an argument and returns a Charset object. The Charset object can then be used to create a new String from the byte array.

```java
Charset charset = Charset.forName("UTF-8");
String str = new String(byteArray, charset);
```
