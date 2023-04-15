---
title: What is the process for creating an md5 hash using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the MessageDigest class from the java.security package to generate an MD5 hash.
---

**Contents**

[TOC]

### Using the MessageDigest Class

The `MessageDigest` class is a part of the Java Cryptography Architecture (JCA) and provides an implementation of the MD5 algorithm.

### Steps
1. Create an instance of the `MessageDigest` class.
```java
MessageDigest md = MessageDigest.getInstance("MD5");
```
2. Update the `MessageDigest` object with the data you want to hash.
```java
md.update(data);
```
3. Generate the hash by calling the `digest()` method.
```java
byte[] digest = md.digest();
```

### Using the Apache Commons Codec Library

The Apache Commons Codec library provides an implementation of the MD5 algorithm.

### Steps
1. Add the Apache Commons Codec library to your project.
2. Create an instance of the `DigestUtils` class.
```java
DigestUtils digestUtils = new DigestUtils();
```
3. Generate the hash by calling the `md5Hex()` method.
```java
String hash = digestUtils.md5Hex(data);
```
