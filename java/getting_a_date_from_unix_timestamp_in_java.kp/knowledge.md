---
title: Obtaining a date object from a unix timestamp in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Date corresponding to a Unix timestamp can be obtained by instantiating a new Date object with the timestamp as the constructor argument.
---

**Contents**

[TOC]

###1. Convert Unix Timestamp to milliseconds

The Unix timestamp value is the number of seconds since January 1, 1970. To convert the Unix timestamp to milliseconds, we can multiply the value by 1000. 

###2. Create Date Object

Once we have the timestamp in milliseconds, we can create a new Date object in Java using the constructor that takes a long value representing the number of milliseconds since the Unix epoch. 

###3. Format Date

Once we have the Date object, we can format it in any way we want, using the SimpleDateFormat class. 

###4. Output Date

Finally, we can output the formatted date using the toString() method of the Date object.
