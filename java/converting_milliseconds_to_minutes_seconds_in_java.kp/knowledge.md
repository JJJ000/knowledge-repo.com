---
title: What is the Java code to convert milliseconds to a format of "x mins, x seconds"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the java.time.Duration class to convert milliseconds to minutes and seconds.
---

**Contents**

[TOC]

### Get Milliseconds

Milliseconds can be obtained by using the `System.currentTimeMillis()` method. This method returns the current time in milliseconds since January 1, 1970. 

### Convert Milliseconds to Seconds

To convert milliseconds to seconds, we can divide the milliseconds by 1000. This will give us the number of seconds since January 1, 1970.

### Convert Seconds to Minutes

To convert seconds to minutes, we can divide the number of seconds by 60. This will give us the number of minutes since January 1, 1970.

### Format Output

Finally, we can use the `String.format()` method to format the output as "X mins, x seconds". This will give us the desired output.
