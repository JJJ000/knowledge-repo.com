---
title: How many days are there between two dates using joda-time?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The number of days between two dates in Joda-Time in Java can be calculated using the Days.daysBetween() method.
---

**Contents**

[TOC]

### Overview
Joda-Time is a Java library for working with date and time objects, and is used for calculating the number of days between two dates.

### How to Calculate
The Joda-Time library provides a method, Days.daysBetween(), which can be used to calculate the number of days between two dates. This method takes two parameters, a start date and an end date, and returns an instance of the Days class, which contains the calculated number of days between the two dates.

### Example Code
The following is an example of how to use the Days.daysBetween() method to calculate the number of days between two dates:

```java
DateTime startDate = new DateTime(2020, 1, 1, 0, 0);
DateTime endDate = new DateTime(2020, 3, 1, 0, 0);
Days daysBetween = Days.daysBetween(startDate, endDate);
int numberOfDays = daysBetween.getDays();
```

### Output
In this example, the output would be 59 days.
