---
title: What is the iso 8601 format for the current date, hour, and minute?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the SimpleDateFormat class to get the current moment in ISO 8601 format with date, hour, and minute in Java.
---

**Contents**

[TOC]

### Using the java.time Package

The java.time package is the standard Java 8 date and time API. It provides several classes for representing date and time, such as `LocalDateTime`, `ZonedDateTime`, and `OffsetDateTime`.

To get the current moment in ISO 8601 format with date, hour, and minute, the `OffsetDateTime` class can be used. The `now()` method of the `OffsetDateTime` class returns the current date and time in the ISO-8601 format. 

```
OffsetDateTime now = OffsetDateTime.now();
String iso8601String = now.toString();
```

### Using the java.util.Date Class

The `java.util.Date` class can also be used to get the current moment in ISO 8601 format with date, hour, and minute. The `Date` class provides the `toString()` method which returns a string representation of the date in ISO 8601 format.

```
Date now = new Date();
String iso8601String = now.toString();
```
