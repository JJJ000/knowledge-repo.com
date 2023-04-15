---
title: How to obtain the digits for months and days of the year from a Python date?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the strftime() function with the format codes %m for the month and %d for the day, as shown in strftime(`%m %d`, date).
---

**Contents**

[TOC]

1. Introduction
When working with dates in Python, it is often necessary to extract specific information, such as double-digit months and days, from the date. This can be done using various methods provided by Python's built-in datetime module.

2. Using strftime() method
One way to extract double-digit months and days from a Python date is to use the strftime() method. This method allows us to format the date as a string using various codes that represent specific date and time information. To extract double-digit months and days, we can use the '%m' and '%d' codes respectively.

```
import datetime

date = datetime.datetime.now()

month = date.strftime('%m')
day = date.strftime('%d')

print(month)
print(day)
```

This code will output the current month and day in double-digit format.

3. Using .month and .day attributes
Another way to extract double-digit months and days from a Python date is to use the .month and .day attributes of the date object. These attributes return integer values representing the month and day respectively, which can be converted to strings with double digits by using the string formatting method.

```
import datetime

date = datetime.datetime.now()

month = '{:02d}'.format(date.month)
day = '{:02d}'.format(date.day)

print(month)
print(day)
```

This code will also output the current month and day in double-digit format.

4. Conclusion
There are various ways to extract double-digit months and days from a Python date, depending on the specific requirements of the code. The strftime() method and .month and .day attributes are two examples of how this can be achieved.
