---
title: Changing from java.time.localdatetime to java.util.date and vice versa
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use java.time.LocalDateTime`s toInstant() method to convert from LocalDateTime to Date, and Date`s toInstant() method to convert from Date to LocalDateTime.
---

**Contents**

[TOC]

### Converting from java.time.LocalDateTime to java.util.Date

To convert from a java.time.LocalDateTime object to a java.util.Date object, you can use the toInstant() method of the LocalDateTime class. This method will return an Instant object, which can then be used to create a Date object using the Date.from() method.

```
LocalDateTime localDateTime = LocalDateTime.now();
Instant instant = localDateTime.toInstant(ZoneOffset.UTC);
Date date = Date.from(instant);
```

### Converting from java.util.Date to java.time.LocalDateTime

To convert from a java.util.Date object to a java.time.LocalDateTime object, you can use the toInstant() method of the Date class. This method will return an Instant object, which can then be used to create a LocalDateTime object using the LocalDateTime.ofInstant() method.

```
Date date = new Date();
Instant instant = date.toInstant();
LocalDateTime localDateTime = LocalDateTime.ofInstant(instant, ZoneOffset.UTC);
```
