---
title: What is the most efficient way to get the current date and time in utc or gmt using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Instant class from the java.time package to get the current date and time in UTC/GMT.
---

**Contents**

[TOC]

1. Using Date and Time API

The new Date and Time API in Java 8 makes it easy to get the current date and time in UTC or GMT. The Instant class in the java.time package represents a moment on the timeline in UTC. The now() method of the Instant class returns the current date and time in UTC.

```java
Instant nowUtc = Instant.now();
```

2. Using Calendar

The Calendar class in the java.util package can be used to get the current date and time in UTC or GMT. The getInstance() method of the Calendar class returns a Calendar object initialized with the current date and time in the default time zone.

To get the current date and time in UTC, the setTimeZone() method of the Calendar class can be used to set the time zone to UTC.

```java
Calendar calendar = Calendar.getInstance();
calendar.setTimeZone(TimeZone.getTimeZone("UTC"));
```

3. Using SimpleDateFormat

The SimpleDateFormat class in the java.text package can be used to get the current date and time in UTC or GMT. The getTimeZone() method of the SimpleDateFormat class can be used to set the time zone to UTC.

```java
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
sdf.setTimeZone(TimeZone.getTimeZone("UTC"));
```

4. Using Joda-Time

The Joda-Time library is a popular library for working with date and time in Java. The DateTime class of the Joda-Time library represents a date and time with millisecond precision in UTC. The DateTime class provides the now() method to get the current date and time in UTC.

```java
DateTime dateTime = DateTime.now(DateTimeZone.UTC);
```
