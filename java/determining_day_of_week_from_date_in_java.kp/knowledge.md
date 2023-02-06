---
title: What is the day of the week for a given date?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The day of the week can be determined by using the LocalDate class in Java and passing in the desired date.
---

**Contents**

[TOC]

# Section 1: Overview

Java provides a wide range of options for determining the day of the week for a given date. This article explains how to use the Calendar and Date classes, as well as the Java 8 Date/Time API, to determine the day of the week for a given date.

# Section 2: Using the Calendar Class

The Calendar class is the most basic and widely used method of determining the day of the week for a given date. The Calendar class has a set() method which can be used to set a date, and the get() method can be used to retrieve the day of the week. The following code snippet shows how to use the Calendar class to determine the day of the week for a given date:

Calendar cal = Calendar.getInstance(); 
cal.set(year, month, day); 
int dayOfWeek = cal.get(Calendar.DAY_OF_WEEK);

# Section 3: Using the Date Class

The Date class is another option for determining the day of the week for a given date. The Date class has a setTime() method which can be used to set a date, and the getDay() method can be used to retrieve the day of the week. The following code snippet shows how to use the Date class to determine the day of the week for a given date:

Date date = new Date(); 
date.setTime(year, month, day); 
int dayOfWeek = date.getDay();

# Section 4: Using the Java 8 Date/Time API

The Java 8 Date/Time API provides a more modern and comprehensive solution for determining the day of the week for a given date. The LocalDate class has a of() method which can be used to set a date, and the getDayOfWeek() method can be used to retrieve the day of the week. The following code snippet shows how to use the Java 8 Date/Time API to determine the day of the week for a given date:

LocalDate date = LocalDate.of(year, month, day); 
DayOfWeek dayOfWeek = date.getDayOfWeek();
