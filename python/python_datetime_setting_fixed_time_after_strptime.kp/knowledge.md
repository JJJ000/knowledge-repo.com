---
title: How to set a fixed hour and minute in Python datetime after using strptime to extract day, month, and year
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Using the datetime.replace() method to set the hour and minute values to a fixed value after parsing day, month and year values using strptime.
---

**Contents**

[TOC]

# Introduction

In Python, the datetime module provides various classes to work with dates and times. To set a fixed hour and minute after using strptime to get day, month, and year, we can take the following approach.

# Step 1: Convert string to datetime object

The first step is to convert the string to a datetime object using the strptime() method. This method takes a string and a format string as input and returns a datetime object.

```python
from datetime import datetime

date_string = '2022-10-22'
format = '%Y-%m-%d'

date_object = datetime.strptime(date_string, format)
```

In this code snippet, we have converted the string `'2022-10-22'` to a datetime object. The `%Y-%m-%d` format string specifies that the year should be represented by four digits, the month should be represented by two digits, and the day should be represented by two digits.

# Step 2: Set fixed hour and minute

The next step is to set a fixed hour and minute for the datetime object. We can do this by creating a new datetime object with the year, month, day, hour, and minute set to the desired values. 

```python
hour = 10
minute = 30

new_date_object = datetime(year=date_object.year, month=date_object.month, day=date_object.day, hour=hour, minute=minute)
```

In this code snippet, we have created a new datetime object with the year, month, and day set to the values of the original datetime object, and the hour and minute set to 10 and 30 respectively.

# Step 3: Print the result

The last step is to print the resulting datetime object. We can do this using the strftime() method, which takes a format string as input and returns a string representation of the datetime object.

```python
new_format = '%Y-%m-%d %H:%M'
result = new_date_object.strftime(new_format)

print(result)
```

In this code snippet, we have created a new format string `' %Y-%m-%d %H:%M'` that includes the year, month, day, hour, and minute, and used it to convert the new datetime object to a string and print it.

# Conclusion

In this article, we have seen how to set a fixed hour and minute for a datetime object after using strptime to get the day, month, and year. We did this by converting the string to a datetime object, setting the hour and minute, and then printing the result using strftime().
