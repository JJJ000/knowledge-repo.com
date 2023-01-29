---
title: What is the most efficient way to convert a byte size into a readable format in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the java.text.NumberFormat class to convert byte size into a human-readable format.
---

**Contents**

[TOC]

#1 Using the FileUtils Class

The Apache Commons IO library provides the `FileUtils` class which contains a static method called `byteCountToDisplaySize` that can be used to convert byte size into a human-readable format. This method takes a `long` value representing the byte size and returns a `String` representing the human-readable format.

Example:
```java
long bytes = 1024;
String humanReadable = FileUtils.byteCountToDisplaySize(bytes);

System.out.println(humanReadable); // prints "1 KB"
```

#2 Manual Conversion

It is also possible to manually convert byte size into a human-readable format. This can be done by dividing the byte size by the appropriate unit and formatting the result as a `String`.

Example:
```java
long bytes = 1024;
long kilobytes = bytes / 1024;
String humanReadable = String.format("%d KB", kilobytes);

System.out.println(humanReadable); // prints "1 KB"
```

#3 Using the DecimalFormat Class

The `DecimalFormat` class can also be used to convert byte size into a human-readable format. This class takes a `String` representing the format and returns a `String` representing the human-readable format.

Example:
```java
long bytes = 1024;
DecimalFormat df = new DecimalFormat("#.##");
String humanReadable = df.format(bytes / 1024) + " KB";

System.out.println(humanReadable); // prints "1 KB"
```
