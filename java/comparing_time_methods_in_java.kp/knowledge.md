---
title: What are the differences between system.currenttimemillis(), new date(), and calendar.getinstance().gettime()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: System.currentTimeMillis() returns the number of milliseconds since January 1, 1970, while new Date() and Calendar.getInstance().getTime() return a Date object representing the current date and time.
---

**Contents**

[TOC]

### System.currentTimeMillis()
`System.currentTimeMillis()` is a static method of the `System` class that returns the current time in milliseconds since January 1, 1970. It is useful for measuring time elapsed since a certain point in time.

### new Date()
`new Date()` is a constructor of the `Date` class that returns a `Date` object representing the current date and time. It is useful for getting the current date and time in a user-friendly format.

### Calendar.getInstance().getTime()
`Calendar.getInstance().getTime()` is a method of the `Calendar` class that returns a `Date` object representing the current date and time. It is useful for getting the current date and time in a user-friendly format.

### Comparison
`System.currentTimeMillis()` and `Calendar.getInstance().getTime()` both return the current time, but `System.currentTimeMillis()` returns the time in milliseconds since January 1, 1970 while `Calendar.getInstance().getTime()` returns a `Date` object representing the current date and time. `new Date()` also returns a `Date` object representing the current date and time.
