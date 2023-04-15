---
title: What are the steps to change the format of a date string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the datetime.datetime.strptime() method to convert a date string to datetime object and then use strftime() method to convert it to a different format.
---

**Contents**

[TOC]

## Introduction

Python provides multiple ways for converting date strings to different formats. In this tutorial, we will discuss two popular ways to achieve this task.

## Method 1 - Using datetime.strptime()

The `datetime` module provides the `strptime()` method for parsing a date string and converting it to a `datetime` object. We can then use the `strftime()` method to convert the `datetime` object to a string in a desired format.

Here's an example:

```python
import datetime

date_str = "2021-09-28"
date_obj = datetime.datetime.strptime(date_str, "%Y-%m-%d")
new_date_str = date_obj.strftime("%d-%m-%Y")
print(new_date_str) # Output: 28-09-2021
```

In the above code, we first import the `datetime` module. Then we define a `date_str` variable with the date in "YYYY-MM-DD" format.

We use the `strptime()` method to parse the `date_str` and convert it to a `datetime` object. The second argument to `strptime()` specifies the format of the date string.

Finally, we use the `strftime()` method to convert the `datetime` object to a string in "DD-MM-YYYY" format.

## Method 2 - Using dateutil.parser.parse()

The `dateutil` module provides the `parser.parse()` method for parsing a date string and converting it to a `datetime` object. We can then use the `strftime()` method to convert the `datetime` object to a string in a desired format.

Here's an example:

```python
from dateutil.parser import parse

date_str = "2021-09-28"
date_obj = parse(date_str)
new_date_str = date_obj.strftime("%d-%m-%Y")
print(new_date_str) # Output: 28-09-2021
```

In the above code, we first import the `parse()` method from the `dateutil.parser` module. Then we define a `date_str` variable with the date in "YYYY-MM-DD" format.

We use the `parse()` method to parse the `date_str` and convert it to a `datetime` object.

Finally, we use the `strftime()` method to convert the `datetime` object to a string in "DD-MM-YYYY" format.

## Conclusion

Both the methods discussed above are easy to use and can be applied to convert date strings to different formats in Python. The choice between them depends upon personal preference and the complexity of the date string being parsed.
