---
title: What is the syntax for obtaining the current time in yyyy-mm-dd hhmisec.millisecond format in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the SimpleDateFormat class to format the current time in the desired format, e.g. `yyyy-MM-dd HHmmss.SSS`.
---

**Contents**

[TOC]

1. Import Necessary Packages
```
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;
```
2. Creating the DateTimeFormatter
```
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss.SSS");
```
3. Get the Current Time
```
LocalDateTime currentTime = LocalDateTime.now();
```
4. Format the Current Time
```
String formattedTime = currentTime.format(formatter);
```
