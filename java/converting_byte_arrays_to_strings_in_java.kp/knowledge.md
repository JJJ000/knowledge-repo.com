---
title: What is the process of converting a byte array to a string and back again?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String constructor that accepts a byte array to convert a byte array to a String, and use the getBytes method of the String class to convert a String to a byte array.
---

**Contents**

[TOC]

### Converting Byte Array to String

1. Create a new String object and pass the byte array and the character encoding to the constructor.

```java
String str = new String(byteArray, StandardCharsets.UTF_8);
```

2. Use the `getBytes()` method of the String class and pass the character encoding to the method.

```java
byte[] byteArray = str.getBytes(StandardCharsets.UTF_8);
```

### Converting String to Byte Array

1. Create a new ByteArrayOutputStream object.

```java
ByteArrayOutputStream baos = new ByteArrayOutputStream();
```

2. Use the `write()` method of the ByteArrayOutputStream class and pass the string and the character encoding to the method.

```java
baos.write(str.getBytes(StandardCharsets.UTF_8));
```

3. Use the `toByteArray()` method of the ByteArrayOutputStream class to get the byte array.

```java
byte[] byteArray = baos.toByteArray();
```
