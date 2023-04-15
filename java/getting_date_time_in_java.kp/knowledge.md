---
title: What is the syntax for obtaining the current date and time in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the LocalDateTime.now() method to get the current date/time in Java.
---

**Contents**

[TOC]

#1 Using java.time

The java.time package provides classes for representing dates and times. To get the current date and time, use the `LocalDateTime.now()` method.

```
LocalDateTime now = LocalDateTime.now();
System.out.println(now);
```

#2 Using java.util.Date

The java.util.Date class is a legacy class that has been replaced by the java.time package. To get the current date and time, use the `Date.getTime()` method.

```
Date date = new Date();
long time = date.getTime();
System.out.println(time);
```

#3 Using Calendar

The java.util.Calendar class provides a way to get the current date and time. To get the current date and time, use the `Calendar.getInstance()` method.

```
Calendar calendar = Calendar.getInstance();
System.out.println(calendar.getTime());
```

#4 Using Joda-Time

Joda-Time is an open source library for manipulating dates and times. To get the current date and time, use the `DateTime.now()` method.

```
DateTime now = DateTime.now();
System.out.println(now);
```
