---
title: What is the Java code to convert the current timestamp to a string in the format "yyyy.mm.dd.hh.mm.ss"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use SimpleDateFormat and the format string `yyyy.MM.dd.HH.mm.ss` to get the current timestamp in string format.
---

**Contents**

[TOC]

### Section 1: Using the Date Class

The following code snippet can be used to get the current timestamp in the desired String format:

```Java
Date date = new Date();
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy.MM.dd.HH.mm.ss");
String timestamp = dateFormat.format(date);
```

### Section 2: Using the Calendar Class

The following code snippet can be used to get the current timestamp in the desired String format:

```Java
Calendar calendar = Calendar.getInstance();
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy.MM.dd.HH.mm.ss");
String timestamp = dateFormat.format(calendar.getTime());
```

### Section 3: Using the Instant Class

The following code snippet can be used to get the current timestamp in the desired String format:

```Java
Instant instant = Instant.now();
SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy.MM.dd.HH.mm.ss");
String timestamp = dateFormat.format(Date.from(instant));
```

### Section 4: Using the LocalDateTime Class

The following code snippet can be used to get the current timestamp in the desired String format:

```Java
LocalDateTime localDateTime = LocalDateTime.now();
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy.MM.dd.HH.mm.ss");
String timestamp = localDateTime.format(formatter);
```
