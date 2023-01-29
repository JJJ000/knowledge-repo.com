---
title: Convert a file to a byte array in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Files.readAllBytes() method to read a file into a byte array.
---

**Contents**

[TOC]

### Using Java 7

The following code snippet uses the `readAllBytes()` method of the `java.nio.file.Files` class to read all the bytes from a file and store them in a byte array:

```java
Path path = Paths.get("file.txt");
byte[] data = Files.readAllBytes(path);
```

### Using Java 8

The following code snippet uses the `Files.readAllBytes()` method of the `java.nio.file.Files` class to read all the bytes from a file and store them in a byte array:

```java
Path path = Paths.get("file.txt");
byte[] data = Files.readAllBytes(path);
```

### Using Java 9

The following code snippet uses the `Files.readAllBytes()` method of the `java.nio.file.Files` class to read all the bytes from a file and store them in a byte array:

```java
Path path = Paths.get("file.txt");
byte[] data = Files.readAllBytes(path);
```

### Using Java 10

The following code snippet uses the `Files.readAllBytes()` method of the `java.nio.file.Files` class to read all the bytes from a file and store them in a byte array:

```java
Path path = Paths.get("file.txt");
byte[] data = Files.readAllBytes(path);
```
