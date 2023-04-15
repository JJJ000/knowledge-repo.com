---
title: Change a java.time.localdate into a java.util.date type
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `LocalDate.atStartOfDay()` method to convert a `LocalDate` into a `java.util.Date` object.
---

**Contents**

[TOC]

### Solution 1

Using `java.time.LocalDate.atStartOfDay()`:

```java
LocalDate localDate = LocalDate.now();
Instant instant = localDate.atStartOfDay().atZone(ZoneId.systemDefault()).toInstant();
Date date = Date.from(instant);
```

### Solution 2

Using `java.time.LocalDate.toEpochDay()`:

```java
LocalDate localDate = LocalDate.now();
long epochDay = localDate.toEpochDay();
Date date = new Date(TimeUnit.DAYS.toMillis(epochDay));
```
