---
title: What is the process for increasing a date by one day?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can add one day to a date in Java by using the Calendar class to add one day to the current date.
---

**Contents**

[TOC]

### Using Java 8 Date/Time API

The Java 8 Date/Time API provides a convenient way to add one day to a date.

1. Create a `LocalDate` object representing the current date:

```java
LocalDate today = LocalDate.now();
```

2. Use the `plusDays` method to add one day to the date:

```java
LocalDate tomorrow = today.plusDays(1);
```

3. Convert the `LocalDate` object to a `Date` object:

```java
Date date = Date.from(tomorrow.atStartOfDay(ZoneId.systemDefault()).toInstant());
```

### Using Calendar

The `Calendar` class can also be used to add one day to a date.

1. Create a `Calendar` object representing the current date:

```java
Calendar calendar = Calendar.getInstance();
```

2. Use the `add` method to add one day to the date:

```java
calendar.add(Calendar.DATE, 1);
```

3. Convert the `Calendar` object to a `Date` object:

```java
Date date = calendar.getTime();
```
