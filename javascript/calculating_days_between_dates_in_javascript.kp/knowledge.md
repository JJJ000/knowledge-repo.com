---
title: What is the difference in days between two dates?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the Date.getTime() method to get the millisecond value of both dates, then subtract the smaller from the larger and divide by 86400000 (the number of milliseconds in one day) to calculate the number of days between the two dates.
---

**Contents**

[TOC]

# Section 1: Understanding the Date Object

In order to calculate the number of days between two dates in Javascript, it is important to understand the Date object. The Date object is a built-in object in Javascript that stores the date and time. It provides several methods for manipulating and formatting dates. 

# Section 2: Calculating the Difference

Once the Date object is understood, calculating the difference between two dates is relatively straightforward. The Date.now() method can be used to get the current date and time in milliseconds since the Unix epoch. This value can then be used to create two Date objects for the two dates that are being compared. 

# Section 3: Subtracting the Dates

Once the two Date objects have been created, the difference between them can be calculated by subtracting the two dates. The result of this subtraction will be the difference in milliseconds between the two dates. 

# Section 4: Calculating the Number of Days

The final step is to convert the difference in milliseconds into the number of days between the two dates. This can be done by dividing the difference in milliseconds by the number of milliseconds in a day (86400000). The result of this calculation will be the number of days between the two dates.
