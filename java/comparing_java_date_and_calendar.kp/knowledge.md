---
title: Differences between Java date and calendar
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Calendar is a more advanced version of the Date class, providing more functionality for manipulating dates.
---

**Contents**

[TOC]

### Date

The Date class in Java is a class that represents a specific instant in time, with millisecond precision. It is used to store and manipulate dates and times in Java. Date objects are immutable, which means that any operation performed on a Date object does not modify the object itself, but instead creates a new Date object with the result of the operation.

### Calendar

The Calendar class in Java is an abstract class that provides methods for converting between a specific instant in time and a set of calendar fields such as YEAR, MONTH, DAY_OF_MONTH, HOUR, and so on, and for manipulating the calendar fields, such as getting the date of the next week. It also provides additional fields and methods for implementing a concrete calendar system.

### Differences

The main difference between Date and Calendar is that Date is used to represent a specific instant in time, while Calendar is used to manipulate and convert between different calendar systems, such as Gregorian, Julian, and so on. 

Another difference is that Date objects are immutable, while Calendar objects are not. This means that any operation performed on a Date object will not modify the object itself, but instead create a new Date object with the result of the operation. On the other hand, any operation performed on a Calendar object will modify the object itself.
