---
title: Changing a string that follows iso 8601 standards into a java.util.date object
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the SimpleDateFormat class to parse the ISO 8601-compliant String into a java.util.Date object.
---

**Contents**

[TOC]

### Overview
ISO 8601 is an international standard for representing dates and times. It is widely used in computer systems, and is a common format for date and time values in web services. The ISO 8601 format consists of a date and time, separated by a "T" character. The date is represented using the yyyy-MM-dd format, and the time is represented using the HH:mm:ss.SSS format.

### Java Date Class
The java.util.Date class is the standard Java class for representing dates and times. It uses a long value to represent the number of milliseconds since the Unix epoch (January 1, 1970).

### Converting ISO 8601 to Date
To convert an ISO 8601-compliant String to a java.util.Date, you can use the SimpleDateFormat class. The SimpleDateFormat class allows you to specify the format of the date and time string, and then use the parse() method to convert it to a Date object.

### Example
For example, to convert the ISO 8601-compliant String "2020-03-22T13:00:00.000" to a java.util.Date, you could use the following code:

```java
String iso8601String = "2020-03-22T13:00:00.000";
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd'T'HH:mm:ss.SSS");
Date date = sdf.parse(iso8601String);
```
