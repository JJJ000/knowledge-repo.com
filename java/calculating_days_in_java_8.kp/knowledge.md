---
title: Determine the number of days between two dates using Java 8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The number of days between two Dates in Java 8 can be calculated using the ChronoUnit.between() method.
---

**Contents**

[TOC]

### Solution

### Step 1: Initialize Date Objects

We can use the `LocalDate` class to create Date objects.

```java
LocalDate startDate = LocalDate.parse("2020-01-15");
LocalDate endDate = LocalDate.parse("2020-02-15");
```

### Step 2: Calculate the Difference

We can use the `until()` method to calculate the difference between two dates.

```java
long daysBetween = startDate.until(endDate, ChronoUnit.DAYS);
```

### Step 3: Output the Result

We can output the result using `System.out.println()`.

```java
System.out.println("Number of days between two dates: " + daysBetween);
```

### Step 4: Run the Program

We can run the program to get the output.

```
Number of days between two dates: 31
```
