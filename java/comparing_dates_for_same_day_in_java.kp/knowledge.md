---
title: Determining if two java.util.dates occur on the same day
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can compare two java.util.Dates using the Date.getDay() method to check if they are in the same day.
---

**Contents**

[TOC]

### 1. Create a Calendar Object

A `Calendar` object can be used to compare two `Date` objects. The `Calendar` class is a built-in utility class in the Java API.

### 2. Set the Calendar to the Date Objects

The `Calendar` object can be set to the two `Date` objects using the `setTime` method. The `setTime` method takes a `Date` object as an argument.

### 3. Compare the Calendar Objects

The `Calendar` objects can then be compared to see if they are in the same day. The `get` methods of the `Calendar` class can be used to get the year, month, and day of the `Date` objects. If the year, month, and day of the two `Calendar` objects are the same, then the `Date` objects are in the same day.

### 4. Get the Time Difference

The `getTimeInMillis` method of the `Calendar` class can be used to get the time difference between the two `Date` objects in milliseconds. If the time difference is less than 24 hours, then the `Date` objects are in the same day.
