---
title: Converting a Java string into a date
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The java.time.LocalDate class can be used to convert a String to a Date object.
---

**Contents**

[TOC]

### Using SimpleDateFormat
SimpleDateFormat is a class in the Java API used for parsing and formatting dates. It is used to convert a String object to a Date object.

### Syntax
```java
SimpleDateFormat sdf = new SimpleDateFormat(String pattern);
Date date = sdf.parse(String dateString);
```

### Example
The following example shows how to use SimpleDateFormat to convert a String to a Date object.

```java
String dateString = "2020-08-15";
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
Date date = sdf.parse(dateString);
System.out.println(date); // Sat Aug 15 00:00:00 GMT 2020
```

### Other Methods
There are other methods available in the Java API for converting a String to a Date object, such as the Date.parse() and DateFormat.parse() methods.
