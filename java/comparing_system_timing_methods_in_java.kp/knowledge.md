---
title: Comparing system.currenttimemillis to system.nanotime
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: System.currentTimeMillis returns the current time in milliseconds since January 1, 1970, while System.nanoTime returns the current time in nanoseconds since some unspecified starting point in the past.
---

**Contents**

[TOC]

### System.currentTimeMillis

System.currentTimeMillis() returns the current time in milliseconds since the epoch (January 1, 1970 00:00:00 GMT). It is useful for measuring elapsed time in applications, as the value never changes and is not affected by time zone or daylight savings time.

### System.nanoTime

System.nanoTime() returns the current time in nanoseconds since the epoch (January 1, 1970 00:00:00 GMT). It is useful for measuring relative time intervals, as the value is not affected by system time changes. However, it is not suitable for measuring absolute time intervals, as the value may not be consistent across different machines.
