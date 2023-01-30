---
title: What is the process for subtracting one day from a date?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the timedelta function from the datetime module to subtract a day from a date in Python.
---

**Contents**

[TOC]

## Using datetime Module
The datetime module of Python offers classes for manipulating dates and times easily. To subtract a day from a date, the timedelta class of the datetime module is used.

## Syntax
The syntax for subtracting a day from a date is as follows: 

`date - datetime.timedelta(days=1)`

## Example
The following example shows how to subtract a day from a date: 

```python
import datetime

# Define a date
date = datetime.date(2020, 10, 20)

# Subtract a day from the date
date - datetime.timedelta(days=1)

# Result
datetime.date(2020, 10, 19)
```

## Output
The output of the above code is `datetime.date(2020, 10, 19)`, which is the date after subtracting a day from the given date.
