---
title: What is the syntax for retrieving the milliseconds from a localdatetime object in Java 8?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `LocalDateTime.get(ChronoField.MILLI\_OF\_SECOND)` method.
---

**Contents**

[TOC]

### Introduction
The LocalDateTime class in Java 8 provides a way to represent a specific date and time. This class does not have a built-in method for retrieving the milliseconds, but this can be done by creating a new object of the `java.time.Instant` class, which represents an instant in time.

### Creating an Instant Object
The `Instant` class can be used to create an object that represents the current date and time in milliseconds. To create an `Instant` object, use the `now()` method of the `Instant` class. This method takes no arguments and returns an `Instant` object that represents the current date and time in milliseconds.

### Converting LocalDateTime to Instant
In order to get the milliseconds from a `LocalDateTime` object, it must first be converted to an `Instant` object. This can be done by using the `atZone()` method of the `LocalDateTime` class. The `atZone()` method takes a `ZoneId` object as an argument and returns an `Instant` object that represents the same date and time as the `LocalDateTime` object.

### Getting the Milliseconds
Once an `Instant` object has been created, the `toEpochMilli()` method can be used to get the milliseconds. The `toEpochMilli()` method takes no arguments and returns a `long` that represents the milliseconds since the Unix epoch.
