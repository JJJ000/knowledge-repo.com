---
title: What is the best way to compare two dates without taking into account the time?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the Date.compareTo() method to compare two Dates without the time portion.
---

**Contents**

[TOC]

1. Using `java.time.LocalDate` 
   
   The `java.time.LocalDate` class provides a method called `isEqual` which can be used to compare two dates without the time portion.
   
   ```java
   LocalDate date1 = LocalDate.of(2019, Month.MAY, 5);
   LocalDate date2 = LocalDate.of(2019, Month.MAY, 6);
   
   boolean isEqual = date1.isEqual(date2);
   ```
   
2. Using `java.util.Date` 

   The `java.util.Date` class provides a method called `compareTo` which can be used to compare two dates without the time portion.
   
   ```java
   Date date1 = new Date(2019, 5, 5);
   Date date2 = new Date(2019, 5, 6);
   
   int compareResult = date1.compareTo(date2);
   ```

3. Using `java.util.Calendar` 

   The `java.util.Calendar` class provides a method called `compareTo` which can be used to compare two dates without the time portion.
   
   ```java
   Calendar date1 = Calendar.getInstance();
   date1.set(2019, 5, 5);
   
   Calendar date2 = Calendar.getInstance();
   date2.set(2019, 5, 6);
   
   int compareResult = date1.compareTo(date2);
   ```

4. Using `java.text.SimpleDateFormat` 

   The `java.text.SimpleDateFormat` class provides a method called `parse` which can be used to parse two dates without the time portion.
   
   ```java
   SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
   
   Date date1 = sdf.parse("2019-05-05");
   Date date2 = sdf.parse("2019-05-06");
   
   int compareResult = date1.compareTo(date2);
   ```
