---
title: Can a function be used to identify the quarter of the year in which a date falls?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, the quarter of a year can be determined using the datetime module in Python by accessing the attribute `quarter` of a datetime object.
---

**Contents**

[TOC]

# Short Answer

Yes, the function to determine which quarter of the year a date is in is available in Python. You can implement it by using the `datetime` module in Python to extract the quarter from the given date.

# Using datetime module

You can use the `datetime` module in Python to extract the quarter from the date. Python datetime module provides the `date` class which can be used to define a date. 

Here's an example code to determine the quarter from a date:

```python
from datetime import date

def get_quarter(date_obj):
    quarter_dict = {1:1, 2:1, 3:1, 4:2, 5:2, 6:2, 7:3, 8:3, 9:3, 10:4, 11:4, 12:4}
    quarter = quarter_dict[(date_obj.month)]
    return quarter

#Test
some_date = date(2021,12,1)
get_quarter(some_date)
```

This code defines a function `get_quarter()` that takes a date object as input and returns the quarter number as output. The function uses a dictionary to map the month number to the appropriate quarter number.

When you call the `get_quarter()` function with a date object, it will return the quarter number for that date. In the above example, `some_date` is set to December 1, 2021, and the `get_quarter()` function returns 4.

You can modify the function to use a different mapping dictionary as per your requirements.

# Conclusion

In conclusion, you can use the `datetime` module in Python to determine the quarter of the year from a given date by defining a function that returns the quarter number based on the month of the date. This function can be easily modified to suit your specific needs.
