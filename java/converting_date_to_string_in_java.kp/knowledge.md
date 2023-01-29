---
title: Transform a java.util.date object into a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the SimpleDateFormat class to format the Date object into a String.
---

**Contents**

[TOC]

### Using SimpleDateFormat

SimpleDateFormat is a class used to format and parse dates in Java. It allows users to specify a custom format for converting a Date object to a String.

### Syntax

The general syntax for using SimpleDateFormat is as follows:

```
SimpleDateFormat sdf = new SimpleDateFormat(pattern);
String dateString = sdf.format(date);
```

Where `pattern` is the format pattern to be used for the conversion, and `date` is the Date object to be converted.

### Example

To convert a Date object to a String in the format "dd/MM/yyyy", the following code can be used:

```
SimpleDateFormat sdf = new SimpleDateFormat("dd/MM/yyyy");
String dateString = sdf.format(date);
```

### Using toString()

The toString() method of the Date class can also be used to convert a Date object to a String. The format of the String returned by toString() is "EEE MMM dd HH:mm:ss zzz yyyy", where "EEE" is the day of the week, "MMM" is the month, "dd" is the day of the month, "HH:mm:ss" is the time, "zzz" is the timezone, and "yyyy" is the year.

### Example

To convert a Date object to a String using toString(), the following code can be used:

```
String dateString = date.toString();
```
