---
title: Find the integer value of the current year in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The integer value of the current year in Java can be obtained using the Calendar.getInstance().get(Calendar.YEAR) method.
---

**Contents**

[TOC]

### Integer Value

The integer value of the current year in Java can be obtained using the `Calendar` class.

### Code

```java
// Get the current year as an int
Calendar calendar = Calendar.getInstance();
int year = calendar.get(Calendar.YEAR);
```

### Output

The output of the code above is the current year as an integer. For example, if the current year is 2020, then the output of the code above would be `2020`.
