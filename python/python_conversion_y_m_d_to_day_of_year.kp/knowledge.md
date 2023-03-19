---
title: How to transform dates in year/month/day format into day of year format using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The datetime module in Python can convert a given date in the format of Year/Month/Day to Day of Year using the strftime() function with the %j format code.
---

**Contents**

[TOC]

## Section 1: Understanding Day of Year

Day of Year (DOY) is the ordinal number that indicates the sequential count of days in a year starting from January 1st. For example, January 1st is DOY 1, February 1st is DOY 32, and December 31st is DOY 365 (or 366 in a leap year).

## Section 2: Converting Year/Month/Day to Day of Year

Python has built-in datetime library that provides various datetime-related functionalities. We can use the datetime library to convert Year/Month/Day to Day of Year.

Here's an example code:

```python
from datetime import datetime

def to_doy(year, month, day):
    date = datetime(year=year, month=month, day=day)
    return date.strftime('%j')
```

In the above code, we are creating a datetime object using year, month, and day inputs. Then, we are formatting the datetime object as the day of the year using the '%j' format code (which returns the day of the year as a zero-padded decimal number).


## Section 3: Testing the Function

Let's test the function using some example inputs.

```python
# Example usage
print(to_doy(2022, 1, 1))  # Output: 001
print(to_doy(2022, 2, 1))  # Output: 032
print(to_doy(2022, 12, 31))  # Output: 365
```

The output should be 001 for January 1st, 032 for February 1st, and 365 for December 31st.

## Section 4: Conclusion

We have learned how to convert Year/Month/Day to Day of Year using Python's built-in datetime library. DOY can be useful for various applications such as calculating seasonal averages, analyzing weather patterns, and more.
