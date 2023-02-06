---
title: Show the current time in a 12-hour clock with am/pm indication
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: System.out.println(new SimpleDateFormat(`hhmm a`).format(new Date()));
---

**Contents**

[TOC]

# Solution

## Using the Date/Time API

The following code snippet uses the Java 8 Date/Time API to print the current time in 12 hour format with AM/PM:

```java
LocalTime localTime = LocalTime.now();
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("hh:mm a");
System.out.println(localTime.format(formatter));
```

## Using SimpleDateFormat

The following code snippet uses the SimpleDateFormat class to print the current time in 12 hour format with AM/PM:

```java
SimpleDateFormat dateFormat = new SimpleDateFormat("hh:mm a");
System.out.println(dateFormat.format(new Date()));
```
