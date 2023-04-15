---
title: What is causing the unusual outcome when subtracting two times from 1927?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Subtracting two times from 1927 in Java is giving a strange result because Java is not designed to handle dates before the year 1970.
---

**Contents**

[TOC]

### Time Format
The time format used in Java is a 24-hour clock, which means that the time is represented as a number from 0 to 23. For example, 8:00 AM is represented as 8 and 8:00 PM is represented as 20.

### Subtracting Times
When subtracting two times in Java, the result is calculated in terms of the number of hours between the two times. For example, subtracting 8:00 AM from 8:00 PM would result in 12 hours. 

### Problem
In 1927, the 24-hour clock was not widely used, so subtracting two times in Java would result in a strange result. For example, subtracting 8:00 AM from 8:00 PM would result in -4 hours, instead of 12 hours. 

### Solution
To avoid this problem, the two times should be converted to the 24-hour clock format before subtracting them. For example, 8:00 AM would be converted to 8 and 8:00 PM would be converted to 20, and then the two times can be subtracted to get the correct result of 12 hours.
