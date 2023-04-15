---
title: What is the most efficient way to generate a Java 8 localdate object from a long epoch time in milliseconds?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can create a Java 8 LocalDate from a long Epoch time in Milliseconds using the LocalDateTime.ofInstant(Instant.ofEpochMilli(longEpochTimeInMilliseconds), ZoneId.systemDefault()) method.
---

**Contents**

[TOC]

### Convert Milliseconds to Seconds

The first step is to convert the given milliseconds to seconds. This can be done by dividing the given milliseconds by 1000.

### Create Instant Object

Next, create an Instant object from the seconds. An Instant object represents a specific moment in time in the GMT timezone.

### Create LocalDate Object

Finally, create a LocalDate object from the Instant object. The LocalDate object represents a date without time or timezone information.

### Get LocalDate

The LocalDate object can be retrieved using the get() method of the Instant object. This will return a LocalDate object with the date and time information from the given epoch time in milliseconds.
