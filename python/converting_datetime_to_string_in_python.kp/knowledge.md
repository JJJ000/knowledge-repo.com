---
title: Transform a datetime object into a string of the date only in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the strftime() method on a datetime object to convert it to a string of date only.
---

**Contents**

[TOC]

### Method 1: Using strftime()
The `strftime()` method of a `datetime` object can be used to convert the object to a string of date only.

Syntax: `datetime.strftime(format)`

Example:
```
import datetime

# Current date
date_today = datetime.datetime.now()

# Print only the date
print(date_today.strftime("%d/%m/%Y"))
```
Output: `03/02/2020`

### Method 2: Using strptime()
The `strptime()` method of the `datetime` module can be used to convert a string to a `datetime` object.

Syntax: `datetime.strptime(date_string, format)`

Example:
```
import datetime

# String of date
date_str = "03/02/2020"

# Convert to datetime object
date_obj = datetime.datetime.strptime(date_str, "%d/%m/%Y")

# Print only the date
print(date_obj.strftime("%d/%m/%Y"))
```
Output: `03/02/2020`

### Method 3: Using date()
The `date()` method of a `datetime` object can be used to convert the object to a string of date only.

Syntax: `datetime.date()`

Example:
```
import datetime

# Current date
date_today = datetime.datetime.now()

# Print only the date
print(date_today.date())
```
Output: `2020-02-03`
