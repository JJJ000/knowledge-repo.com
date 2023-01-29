---
title: What are the differences between two localdatetime objects in Java 8, expressed in multiple units?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The difference between two LocalDateTime objects can be calculated using the Duration class, which provides methods to get the difference between two LocalDateTime objects in multiple units such as days, hours, minutes, and seconds.
---

**Contents**

[TOC]

`**` Finding the Difference**

The difference between two LocalDateTime objects can be found using the `LocalDateTime.until()` method. This method takes two parameters - the first being the `LocalDateTime` object to which the difference is being calculated and the second being a `TemporalUnit` object which defines the unit in which the difference will be returned. 

`**` TemporalUnit Object**

The `TemporalUnit` object is an interface which is implemented by various classes such as `ChronoUnit`, `IsoFields`, `WeekFields` etc. Each of these classes have constants which correspond to different units of time (e.g. days, weeks, months, etc). 

`**` Getting the Difference**

Once the `TemporalUnit` object has been created, the `LocalDateTime.until()` method can be used to get the difference between two `LocalDateTime` objects. This method will return the difference in the specified unit of time. 

`**` Example**

For example, the following code will calculate the difference between two `LocalDateTime` objects in days:

```
LocalDateTime firstDate = LocalDateTime.of(2020, 1, 1, 0, 0);
LocalDateTime secondDate = LocalDateTime.of(2020, 1, 15, 0, 0);

long difference = firstDate.until(secondDate, ChronoUnit.DAYS);

System.out.println(difference); // prints 14
```
