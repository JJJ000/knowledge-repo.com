---
title: Change a string representation of a date into a timestamp in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the datetime.strptime() function to convert a string date to a timestamp in Python.
---

**Contents**

[TOC]

# Section 1 - Using datetime Module

The datetime module can be used to convert string dates to timestamps. To do this, the datetime.strptime() method can be used. This method takes two arguments: the string date and the format of the string date. For example, to convert the string date "2020-04-30" to a timestamp:

```
import datetime

string_date = "2020-04-30"
date_object = datetime.datetime.strptime(string_date, "%Y-%m-%d")
timestamp = date_object.timestamp()
```

# Section 2 - Using time Module

The time module can be used to convert string dates to timestamps. To do this, the time.strptime() method can be used. This method takes two arguments: the string date and the format of the string date. For example, to convert the string date "2020-04-30" to a timestamp:

```
import time

string_date = "2020-04-30"
date_object = time.strptime(string_date, "%Y-%m-%d")
timestamp = time.mktime(date_object)
```

# Section 3 - Using calendar Module

The calendar module can also be used to convert string dates to timestamps. To do this, the calendar.timegm() method can be used. This method takes one argument: the string date. For example, to convert the string date "2020-04-30" to a timestamp:

```
import calendar

string_date = "2020-04-30"
timestamp = calendar.timegm(time.strptime(string_date, "%Y-%m-%d"))
```

# Section 4 - Using dateutil Module

The dateutil module can also be used to convert string dates to timestamps. To do this, the dateutil.parser.parse() method can be used. This method takes one argument: the string date. For example, to convert the string date "2020-04-30" to a timestamp:

```
import dateutil.parser

string_date = "2020-04-30"
date_object = dateutil.parser.parse(string_date)
timestamp = date_object.timestamp()
```
