---
title: What is the method to maintain the timezone while parsing date/time strings with strptime()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `pytz` module to explicitly set the timezone after parsing the date/time string with `strptime()`.
---

**Contents**

[TOC]

# Introduction

Python provides a built-in function called `strptime()` that can be used to parse a datetime string and convert it into a datetime object. However, when using `strptime()`, the timezone information present in the input string is often lost. In this article, we will discuss how to preserve timezone when parsing date/time strings with `strptime()` in Python.

# Section 1: Understanding the problem

When parsing a datetime string using `strptime()`, the resulting datetime object does not preserve the timezone information. This is because `strptime()` assumes the datetime string to be in the system's local timezone, and converts it to UTC before creating a datetime object. Therefore, any timezone information present in the input string will be lost.

# Section 2: Using dateutil

To preserve the timezone information while parsing a datetime string, we can use the `dateutil` library. This library provides a `parse()` function that can parse a datetime string and create a datetime object with timezone information preserved.

Here's an example:

```
from dateutil import parser

dt_string = "2022-01-01T00:00:00+01:00"
dt_object = parser.parse(dt_string)

print(dt_object)
```

Output:

```
2022-01-01 00:00:00+01:00
```

In the example above, we first import the `parser` function from the `dateutil` library. We then define a datetime string with timezone information, and pass it to the `parse()` function. The function returns a datetime object with the timezone information preserved.

# Section 3: Using pytz

Another way to preserve the timezone information while parsing a datetime string is to use the `pytz` library. This library provides a `timezone()` function that can be used to create a timezone object from a timezone string.

Here's an example:

```
from datetime import datetime
import pytz

tz_string = "Europe/Berlin"
dt_string = "2022-01-01T00:00:00+01:00"

tz = pytz.timezone(tz_string)
dt_object = datetime.strptime(dt_string, '%Y-%m-%dT%H:%M:%S%z').replace(tzinfo=tz)

print(dt_object)
```

Output:

```
2022-01-01 00:00:00+01:00
```

In the example above, we first import the `datetime` module and the `pytz` library. We then define a timezone string and a datetime string with timezone information. We use the `timezone()` function from `pytz` to create a timezone object from the timezone string. We then use `strptime()` function to parse the datetime string, and replace the timezone information using the `replace()` method. Finally, we get a datetime object with the timezone information preserved.

# Conclusion

In this article, we have discussed how to preserve timezone information when parsing datetime strings using `strptime()` in Python. We have seen two different ways to achieve this - using the `dateutil` library and using the `pytz` library. Both methods allow us to create datetime objects with timezone information, and are therefore useful in situations where timezone information is important.
