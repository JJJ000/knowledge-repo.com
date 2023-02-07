---
title: Converting JSON date and time between Python and javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The ISO 8601 standard can be used to ensure compatibility between Python and JavaScript when dealing with datetime.
---

**Contents**

[TOC]

### JavaScript Date

In JavaScript, the Date object is used to represent a date and time. It provides several methods for manipulating and formatting dates and times.

### JSON Date Format

JSON supports the ISO 8601 date format, which is a standard for representing dates and times. The format is as follows:

`yyyy-MM-ddTHH:mm:ss.sssZ`

where `yyyy` is the four-digit year, `MM` is the two-digit month (01-12), `dd` is the two-digit day (01-31), `HH` is the two-digit hour (00-23), `mm` is the two-digit minute (00-59), `ss` is the two-digit second (00-59), and `sss` is the three-digit millisecond (000-999). The `Z` indicates that the time is in UTC (Coordinated Universal Time).

### Python Date Format

Python also supports the ISO 8601 date format. The format is as follows:

`%Y-%m-%dT%H:%M:%S.%fZ`

where `%Y` is the four-digit year, `%m` is the two-digit month (01-12), `%d` is the two-digit day (01-31), `%H` is the two-digit hour (00-23), `%M` is the two-digit minute (00-59), `%S` is the two-digit second (00-59), and `%f` is the six-digit microsecond (000000-999999). The `Z` indicates that the time is in UTC (Coordinated Universal Time).

### Conversion

To convert between the two formats, you can use the `strftime` and `strptime` methods in Python and the `toISOString` and `Date.parse` methods in JavaScript.
