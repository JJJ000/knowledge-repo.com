---
title: What is the syntax for obtaining a "timezone aware" datetime.today() value in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You should use the datetime.now(tz=pytz.timezone(`timezone\_name`)) function to get a timezone aware value of datetime.today().
---

**Contents**

[TOC]

# Section 1: Understanding Timezone Awareness

Timezone awareness is the concept of being aware of the time zone in which a particular date or time falls. It is important to be aware of the time zone when dealing with dates and times, as different time zones may have different rules and regulations regarding how dates and times should be handled.

# Section 2: Using datetime.today()

In Python, the datetime.today() function can be used to get the current date and time in the local timezone. This function is not timezone aware, however, so if you need to get the current date and time in a different timezone, you will need to use a different function.

# Section 3: Getting Timezone Aware Values

To get a value of datetime.today() that is timezone aware, you can use the pytz library. This library allows you to specify the timezone you would like to use, and it will return the current date and time in that timezone.

# Section 4: Example

For example, to get the current date and time in the Central European Timezone, you could use the following code:

```
import pytz

central_european_timezone = pytz.timezone("Europe/Berlin")
date_time_in_cet = datetime.now(central_european_timezone)
```
