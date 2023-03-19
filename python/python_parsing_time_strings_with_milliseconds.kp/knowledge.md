---
title: What is the method to parse a time string that has milliseconds in it using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the datetime module`s strptime() method with the appropriate format code for milliseconds (%f).
---

**Contents**

[TOC]

## Section 1: Understanding the time module in Python

Before we jump into parsing a time string with milliseconds in Python, it's important to understand the time module in Python. The time module provides functions to work with time-related tasks, such as converting between different time representations, measuring time elapsed, and delaying code execution.

Here are some of the most common functions that the time module provides:

- `time.time()`: returns the current timestamp as a float value representing the number of seconds since the epoch (January 1, 1970, 00:00:00 UTC).
- `time.localtime([timestamp])`: converts a timestamp to a time struct containing various time attributes (year, month, day, hour, minute, second, day of the week, day of the year, daylight saving time).
- `time.strftime(format, [time_struct])`: converts a time struct to a formatted string based on a given format string.

With these functions in mind, let's move on to parsing a time string containing milliseconds in Python. 

## Section 2: Parsing a time string with milliseconds in Python

To parse a time string with milliseconds in Python, we can make use of the datetime module, which provides a more robust way of parsing and manipulating date and time values.

Here's an example code snippet that demonstrates how to parse a time string with milliseconds:

```python
from datetime import datetime

time_str = "2021-07-26 14:34:12.345"
datetime_obj = datetime.strptime(time_str, '%Y-%m-%d %H:%M:%S.%f')
```

In the above code, we first import the datetime class from the datetime module. We then define a time string that contains milliseconds, which is in the format of `%Y-%m-%d %H:%M:%S.%f` (where `%f` represents the microseconds). Finally, we use the `datetime.strptime()` function to parse the time string into a datetime object.

Once we have a datetime object, we can access various attributes of the time value, such as the year, month, day, hour, minute, second, and microsecond, using the `.year`, `.month`, `.day`, `.hour`, `.minute`, `.second`, and `.microsecond` properties, respectively.

## Section 3: Converting a datetime object to a timestamp with milliseconds

If we want to convert a datetime object to a timestamp with milliseconds, we can use the `datetime.timestamp()` method, which returns the POSIX timestamp (number of seconds since January 1, 1970, 00:00:00 UTC) as a floating-point number.

Here's an example code snippet that demonstrates how to convert a datetime object to a timestamp with milliseconds:

```python
timestamp = datetime_obj.timestamp() * 1000.0
```

In the above code, we call the `datetime_obj.timestamp()` method to get the POSIX timestamp in seconds, and then multiply it by 1000.0 to convert it to milliseconds.

## Section 4: Conclusion

In this quick guide, we covered how to parse a time string containing milliseconds in Python using the datetime module. We used the `datetime.strptime()` function to parse the time string into a datetime object, and then showed how to convert a datetime object to a timestamp with milliseconds using the `datetime.timestamp()` method. With this knowledge, you should be able to work with time values in Python that contain milliseconds.
