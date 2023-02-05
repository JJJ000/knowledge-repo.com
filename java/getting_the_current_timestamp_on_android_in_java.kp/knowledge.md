---
title: What is the current timestamp on an Android device?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The current timestamp in Java can be obtained using the System.currentTimeMillis() method.
---

**Contents**

[TOC]

## Section 1: Find Current Timestamp

The current timestamp in Java can be found using the `System.currentTimeMillis()` method. This method returns the current time in milliseconds since the Unix epoch (January 1, 1970 00:00:00 GMT).

## Section 2: Convert Timestamp to Date

The timestamp can be converted to a `java.util.Date` object by using the `new Date(long timestamp)` constructor. This Date object can then be used to format the timestamp into different date formats.

## Section 3: Format Timestamp

The timestamp can be formatted into different date formats using the `SimpleDateFormat` class. This class provides a variety of methods for formatting and parsing dates.

## Section 4: Example

The following example code demonstrates how to get the current timestamp and format it into a date string:

```java
// Get current timestamp
long timestamp = System.currentTimeMillis();

// Create a Date object from the timestamp
Date date = new Date(timestamp);

// Create a SimpleDateFormat object for formatting the date
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");

// Format the timestamp into a date string
String dateString = sdf.format(date);

// Print the date string
System.out.println(dateString);
```
