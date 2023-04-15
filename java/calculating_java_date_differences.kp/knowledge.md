---
title: Finding the interval between two Java date objects
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The difference between two Java date instances can be calculated using the Date.getTime() method.
---

**Contents**

[TOC]

### Section 1 - Create Date Instances 

Create two date instances, one for the current date and one for a past date.

```java
// Create current date instance
Date currentDate = new Date();

// Create past date instance
Date pastDate = new Date(1545, 11, 2);
```

### Section 2 - Calculate Difference

Calculate the difference between the two date instances in milliseconds.

```java
// Calculate difference in milliseconds
long difference = currentDate.getTime() - pastDate.getTime();
```

### Section 3 - Format Difference

Format the difference into days, hours, minutes, and seconds.

```java
// Calculate difference in days
long diffInDays = TimeUnit.MILLISECONDS.toDays(difference);

// Calculate difference in hours
long diffInHours = TimeUnit.MILLISECONDS.toHours(difference);

// Calculate difference in minutes
long diffInMinutes = TimeUnit.MILLISECONDS.toMinutes(difference);

// Calculate difference in seconds
long diffInSeconds = TimeUnit.MILLISECONDS.toSeconds(difference);
```

### Section 4 - Output

Output the difference in the desired format.

```java
// Output difference
System.out.println("Difference is " + diffInDays + " days, " + diffInHours + " hours, " + diffInMinutes + " minutes, and " + diffInSeconds + " seconds.");
```
