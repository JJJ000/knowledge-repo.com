---
title: What is the process of creating a timedelta object using a basic string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `datetime.timedelta` function, passing in the appropriate values for hours, minutes, seconds, microseconds, and/or days.
---

**Contents**

[TOC]

## Split the string into components

The first step in constructing a timedelta object from a string is to split the string into its component parts. A typical format for a timedelta string might be '4 days, 6 hours and 42 minutes'. To get the individual components of this string, we can use Python's built-in `split()` method, which splits a string at a specified delimiter and returns a list of strings.

``` python
time_string = '4 days, 6 hours and 42 minutes'
components = time_string.split(', ')
```

In this example, we use `', '` as the delimiter to split the string into a list of component strings.

## Parse the component strings into timedelta values

Once we have the components of the string, we can parse them into `timedelta` values. We can do this by iterating over the components list and using regular expressions to extract the numerical values and units of time. We can then use these values to create a new `timedelta` object for each component. 

``` python
import re
from datetime import timedelta

components = ['4 days', '6 hours', '42 minutes']

pattern = re.compile(r'(\d+) (\w+)')

timedeltas = []
for component in components:
    match = pattern.match(component)
    if match:
        num = int(match.group(1))
        unit = match.group(2)
        if unit == 'days':
            timedeltas.append(timedelta(days=num))
        elif unit == 'hours':
            timedeltas.append(timedelta(hours=num))
        elif unit == 'minutes':
            timedeltas.append(timedelta(minutes=num))
```

In this example, we use a regular expression pattern to extract the numeric value and unit of time from each component string. We then use a series of if statements to determine which `timedelta` constructor to use based on the unit of time.

## Combine the timedelta values

Finally, we can combine the `timedelta` values for each component into a single `timedelta` object. We can do this by using Python's built-in `sum()` function to add together all the `timedelta` objects in the `timedeltas` list.

``` python
total_time = sum(timedeltas)
```

In this example, `total_time` will be a `timedelta` object representing the total time specified in the original string. 

## Full code

Putting it all together, here's the full code to construct a `timedelta` object from a string:

``` python
import re
from datetime import timedelta

time_string = '4 days, 6 hours and 42 minutes'
components = time_string.split(', ')

pattern = re.compile(r'(\d+) (\w+)')

timedeltas = []
for component in components:
    match = pattern.match(component)
    if match:
        num = int(match.group(1))
        unit = match.group(2)
        if unit == 'days':
            timedeltas.append(timedelta(days=num))
        elif unit == 'hours':
            timedeltas.append(timedelta(hours=num))
        elif unit == 'minutes':
            timedeltas.append(timedelta(minutes=num))

total_time = sum(timedeltas)
```

This code will work for any string that follows the format of 'X units of time, Y units of time, and Z units of time', where units of time can be 'days', 'hours', or 'minutes'. If you need to parse different formats, you may need to adjust the regular expression pattern or the logic for parsing the components.
