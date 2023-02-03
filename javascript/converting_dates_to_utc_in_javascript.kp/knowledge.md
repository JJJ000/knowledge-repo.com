---
title: What is the process for converting a date to utc?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the .getTime() method to convert a Date to UTC in Javascript.
---

**Contents**

[TOC]

# Section 1 - Understanding UTC
UTC stands for Coordinated Universal Time and is the primary time standard by which the world regulates clocks and time. It is equivalent to Greenwich Mean Time (GMT).

# Section 2 - Converting to UTC
In JavaScript, the Date object provides a number of methods for working with dates and times. The `getTime()` method can be used to convert a date to milliseconds since the Unix Epoch. This can then be used to convert a date to UTC by adding the UTC offset. 

# Section 3 - Calculating UTC Offset
The UTC offset can be calculated using the `getTimezoneOffset()` method of the Date object. This method returns the timezone offset from UTC, in minutes.

# Section 4 - Putting it Together
To convert a date to UTC, use the following steps:

1. Create a Date object for the date to be converted
2. Use the `getTime()` method to convert the Date object to milliseconds
3. Use the `getTimezoneOffset()` method to calculate the UTC offset
4. Add the UTC offset to the milliseconds from step 2 to get the UTC milliseconds
5. Create a new Date object using the UTC milliseconds from step 4
