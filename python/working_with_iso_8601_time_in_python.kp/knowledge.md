---
title: How to work with iso 8601 formatted time in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The datetime module in Python can be used to work with ISO 8601 formatted dates and times.
---

**Contents**

[TOC]

# Introduction

ISO 8601 is an international standard for representing dates and times. It is a widely used format for representing dates and times in many different applications, including Python.

# Format

The ISO 8601 format consists of a date followed by a time, both of which are composed of numbers. The date is written in the form YYYY-MM-DD, where YYYY is the year, MM is the month, and DD is the day. The time is written in the form hh:mm:ss, where hh is the hour, mm is the minute, and ss is the second.

# Python Implementation

In Python, the ISO 8601 format can be represented using the datetime module. The datetime.datetime class can be used to represent a date and time in the ISO 8601 format. The class can be initialized with a string in the ISO 8601 format, or with individual year, month, day, hour, minute, and second values.

# Example

Here is an example of how to create a datetime object in the ISO 8601 format in Python:

```
import datetime

# Create a datetime object from a string in ISO 8601 format
date_time_str = '2020-06-30T12:34:56'
date_time_obj = datetime.datetime.strptime(date_time_str, '%Y-%m-%dT%H:%M:%S')

# Create a datetime object from individual year, month, day, hour, minute, and second values
date_time_obj = datetime.datetime(2020, 6, 30, 12, 34, 56)
```
