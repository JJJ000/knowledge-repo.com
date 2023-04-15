---
title: What does the date 2011-08-12t201746.384z represent?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This date format is the ISO 8601 standard for representing dates and times in Java.
---

**Contents**

[TOC]

### ISO 8601

2011-08-12T20:17:46.384Z is an example of the ISO 8601 date format. This format is used to represent dates and times in a machine-readable way.

### Java

In Java, this date format can be parsed using the [`ZonedDateTime` class](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/time/ZonedDateTime.html).

```java
ZonedDateTime zdt = ZonedDateTime.parse("2011-08-12T20:17:46.384Z");
```

### Output

The parsed `ZonedDateTime` can be output in a variety of formats, such as:

```java
System.out.println(zdt.toLocalDateTime()); // 2011-08-12T20:17:46.384
System.out.println(zdt.toLocalDate()); // 2011-08-12
System.out.println(zdt.toLocalTime()); // 20:17:46.384
```
