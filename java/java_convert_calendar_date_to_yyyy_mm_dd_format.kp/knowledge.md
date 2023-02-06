---
title: Convert a calendar date to the yyyy-mm-dd format in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The date can be converted to yyyy-MM-dd format using the SimpleDateFormat class and the pattern `yyyy-MM-dd`.
---

**Contents**

[TOC]

# Section 1: Overview

The task of converting a java.util.Calendar date to the format yyyy-MM-dd is a relatively straightforward process. It involves extracting the year, month and day values from the Calendar object and formatting them into a string that follows the yyyy-MM-dd format.

# Section 2: Extracting the Date Values

The Calendar class provides several methods for extracting the year, month and day values from a Calendar object. These methods are `get(Calendar.YEAR)`, `get(Calendar.MONTH)` and `get(Calendar.DAY_OF_MONTH)` respectively. These methods return the values as integers, which will need to be formatted into a string.

# Section 3: Formatting the Date Values

The date values can be formatted into a string using the `String.format()` method. This method accepts a format string, which specifies how the values should be formatted. For example, the following format string will format the date values into a string that follows the yyyy-MM-dd format: `"%04d-%02d-%02d"`.

# Section 4: Putting it All Together

The following code snippet demonstrates how to convert a java.util.Calendar date to the format yyyy-MM-dd:

```java
Calendar date = Calendar.getInstance();
String formattedDate = String.format("%04d-%02d-%02d", 
    date.get(Calendar.YEAR), 
    date.get(Calendar.MONTH), 
    date.get(Calendar.DAY_OF_MONTH));
```
