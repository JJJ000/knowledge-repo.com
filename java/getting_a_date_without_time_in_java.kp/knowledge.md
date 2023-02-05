---
title: What is the syntax for creating a date object without a time component in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the LocalDate class to get a Date without time in Java.
---

**Contents**

[TOC]

## Step 1: Create an Instance of Date

Create an instance of the Date class. This will set the date to the current date and time.

```
Date date = new Date();
```

## Step 2: Create an Instance of Calendar

Create an instance of the Calendar class. This will allow us to manipulate the date and time.

```
Calendar cal = Calendar.getInstance();
```

## Step 3: Set the Calendar to the Date

Set the calendar instance to the date instance.

```
cal.setTime(date);
```

## Step 4: Set the Time to 0

Set the time to 0 so that the date will not contain a time.

```
cal.set(Calendar.HOUR_OF_DAY, 0);
cal.set(Calendar.MINUTE, 0);
cal.set(Calendar.SECOND, 0);
cal.set(Calendar.MILLISECOND, 0);
```

## Step 5: Get the Date Without Time

Finally, get the date without time by getting the time from the calendar instance.

```
Date dateWithoutTime = cal.getTime();
```
