---
title: The iso format of a utc datetime object in Python does not incorporate z (zulu or zero offset)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: UTC datetime objects in Python`s ISO format do include `Z` to represent the Zero offset or Zulu time zone.
---

**Contents**

[TOC]

Background
-----------

Python's `datetime` module is used to represent dates and times in Python. The module provides various classes to represent different types of date and time information, such as the `date` class to represent dates, the `time` class to represent times, and the `datetime` class to represent both dates and times. 

One of the most common date and time formats used for representing UTC times is the ISO 8601 format. This format includes the letter "Z" at the end of the string to indicate that the time is in UTC (also known as "Zulu" or "Zero" offset). For example, "2022-01-01T00:00:00Z" represents midnight on January 1, 2022, in UTC.

Issue
-----

When using Python's `datetime` module to create a `datetime` object representing a UTC time, the ISO format string returned by the `isoformat()` method does not include the "Z" character to denote the UTC offset.

Solution
--------

To add the "Z" character to the end of the ISO format string, you can use the `strftime()` method instead of the `isoformat()` method. The `strftime()` method allows you to specify the format string used to represent the date and time.

```python
>>> from datetime import datetime
>>> now = datetime.utcnow()
>>> now.strftime('%Y-%m-%dT%H:%M:%SZ')
'2022-08-22T10:00:00Z'
```

In the format string used for `strftime()`, `%Z` represents the name of the time zone, which is not appropriate for UTC times. Instead, use the literal "Z" to indicate the UTC offset.

Alternatively, you can manually append the "Z" character to the end of the ISO format string returned by `isoformat()`.

```python
>>> now.isoformat() + 'Z'
'2022-08-22T10:00:00.000000Z'
```

This will append the "Z" character to the end of the ISO format string, but note that it will also include microseconds and trailing zeroes that are not included in the standard ISO format string.
