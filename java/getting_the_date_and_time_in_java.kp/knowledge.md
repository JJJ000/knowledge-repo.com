---
title: What is the current date and time?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The current date and time can be retrieved using the LocalDateTime.now() method.
---

**Contents**

[TOC]

### Using the Date Class

The Date class in Java provides a way to get the current date and time. To use this class, the following code can be used:

```java
Date date = new Date();
System.out.println(date);
```

This will print out the current date and time in the following format: `Thu Aug 13 10:20:56 EDT 2020`.

### Using the Calendar Class

The Calendar class in Java provides a way to get the current date and time. To use this class, the following code can be used:

```java
Calendar calendar = Calendar.getInstance();
System.out.println(calendar.getTime());
```

This will print out the current date and time in the following format: `Thu Aug 13 10:20:56 EDT 2020`.

### Using the LocalDateTime Class

The LocalDateTime class in Java provides a way to get the current date and time. To use this class, the following code can be used:

```java
LocalDateTime localDateTime = LocalDateTime.now();
System.out.println(localDateTime);
```

This will print out the current date and time in the following format: `2020-08-13T10:20:56.935`.

### Using the Instant Class

The Instant class in Java provides a way to get the current date and time. To use this class, the following code can be used:

```java
Instant instant = Instant.now();
System.out.println(instant);
```

This will print out the current date and time in the following format: `2020-08-13T10:20:56.935Z`.
