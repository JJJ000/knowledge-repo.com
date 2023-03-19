---
title: Perform the subtraction of two values twice using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can subtract two times in Python by simply subtracting one datetime object from another datetime object.
---

**Contents**

[TOC]

# Introduction
In Python, subtracting two times can be accomplished using the built-in datetime module. In this article, we will explore how to subtract two times in Python step by step.

# Convert Strings to Datetime Objects
Before we subtract two times, we need to convert the strings representing the times to datetime objects. This can be done using the `strptime` method of the datetime module.

``` python
import datetime

time1_str = "2022-08-01 08:30:00"
time2_str = "2022-08-01 09:00:00"

time1 = datetime.datetime.strptime(time1_str, "%Y-%m-%d %H:%M:%S")
time2 = datetime.datetime.strptime(time2_str, "%Y-%m-%d %H:%M:%S")
```

# Subtract Two Datetime Objects
Now that we have converted the strings to datetime objects, we can subtract them to get the time difference. This can be done simply by subtracting the two datetime objects.

``` python
time_diff = time2 - time1
```

# Display the Time Difference
We can now display the time difference in whatever format we desire. For example, if we wanted to display the time difference in minutes and seconds, we could use the following code.

``` python
time_diff_minutes = time_diff.seconds // 60
time_diff_seconds = time_diff.seconds % 60

print("Time difference: {} minutes and {} seconds".format(time_diff_minutes, time_diff_seconds))
```

This would output: `Time difference: 30 minutes and 0 seconds`

# Conclusion
Subtracting two times in Python is straightforward using the datetime module. By converting the times to datetime objects and subtracting them, we can get the time difference in a variety of formats.
