---
title: What is the syntax for increasing a date by one day in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the LocalDate class from the java.time package and call the plusDays() method with an argument of 1.
---

**Contents**

[TOC]

1. **Using LocalDate Class**

The java.time.LocalDate class is used to represent a date without time-zone information. This class provides various methods to manipulate the date. To increment a date by one day, we can use the plusDays() method of the LocalDate class.

Syntax:

LocalDate.plusDays(long daysToAdd)

Example:

LocalDate currentDate = LocalDate.of(2020, 10, 10); 
LocalDate nextDate = currentDate.plusDays(1);

2. **Using Calendar Class**

The java.util.Calendar class is used to manipulate date and time information. To increment a date by one day, we can use the add() method of the Calendar class.

Syntax:

calendar.add(Calendar.DATE, 1)

Example:

Calendar cal = Calendar.getInstance(); 
cal.set(2020, 10, 10); 
cal.add(Calendar.DATE, 1); 
Date nextDate = cal.getTime();

3. **Using Date Class**

The java.util.Date class represents a specific moment in time. To increment a date by one day, we can use the setTime() method of the Date class.

Syntax:

date.setTime(date.getTime() + (1000 * 60 * 60 * 24));

Example:

Date currentDate = new Date(2020, 10, 10); 
currentDate.setTime(currentDate.getTime() + (1000 * 60 * 60 * 24)); 
Date nextDate = currentDate;

4. **Using Joda Time Library**

The Joda-Time library is an open source date and time library for Java. To increment a date by one day, we can use the plusDays() method of the DateTime class.

Syntax:

dateTime.plusDays(long days)

Example:

DateTime currentDate = new DateTime(2020, 10, 10, 0, 0); 
DateTime nextDate = currentDate.plusDays(1);
