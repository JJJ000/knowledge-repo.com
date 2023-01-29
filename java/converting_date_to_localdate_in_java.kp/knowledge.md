---
title: Transform java.util.date into java.time.localdate
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the LocalDate.ofInstant(date.toInstant(), ZoneId.systemDefault()) method to convert a java.util.Date to a java.time.LocalDate.
---

**Contents**

[TOC]

### Solution 1:
Using `java.time.Instant`:

```java
import java.time.Instant;
import java.time.LocalDate;
import java.util.Date;

public class DateConverter {
    public static LocalDate toLocalDate(Date date) {
        Instant instant = date.toInstant();
        return instant.atZone(ZoneId.systemDefault()).toLocalDate();
    }
}
```

### Solution 2:
Using `java.time.LocalDateTime`:

```java
import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.ZoneId;
import java.util.Date;

public class DateConverter {
    public static LocalDate toLocalDate(Date date) {
        LocalDateTime localDateTime = LocalDateTime.ofInstant(date.toInstant(), ZoneId.systemDefault());
        return localDateTime.toLocalDate();
    }
}
```
