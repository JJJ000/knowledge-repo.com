---
title: What is the process for transforming an integer timestamp into a datetime?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `datetime.fromtimestamp` method with the integer timestamp as its argument to convert it into a datetime object in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, timestamps are represented as integers that represent the number of seconds or nanoseconds (depending on the precision of the timestamp) since January 1, 1970, at 00:00:00 UTC. Converting these integer timestamps to a datetime object is a common task in data analysis and other applications.

Section 2: Using the datetime module
The datetime module in Python provides the ability to work with dates and times. It includes a class called datetime, which can be used to represent a specific date and time.

To convert an integer timestamp into a datetime object, we can use the fromtimestamp() method of the datetime class. This method accepts a Unix timestamp as an argument and returns a corresponding datetime object.

Here's an example:

```
import datetime

timestamp = 1619540799 # Replace with your own timestamp
dt_object = datetime.datetime.fromtimestamp(timestamp)

print("Datetime object:", dt_object)
```

This code will output the datetime object that corresponds to the input timestamp.

Section 3: Timestamp precision
It's worth noting that the fromtimestamp() method assumes that the input timestamp is in seconds. If your timestamp is in milliseconds or microseconds, you'll need to divide it by 1000 or 1000000, respectively, before passing it to the method.

For example, if your input timestamp is in milliseconds, you can convert it to a datetime object like this:

```
import datetime

timestamp_ms = 1619540799000 # Replace with your own timestamp in milliseconds
timestamp_s = timestamp_ms / 1000
dt_object = datetime.datetime.fromtimestamp(timestamp_s)

print("Datetime object:", dt_object)
```

This code first divides the input timestamp by 1000 to convert it from milliseconds to seconds, and then passes the result to the fromtimestamp() method.

Section 4: Conclusion
Converting an integer timestamp to a datetime object in Python is easy with the datetime module's fromtimestamp() method. Remember to divide your timestamp by 1000 or 1000000 if it's in milliseconds or microseconds, respectively.
