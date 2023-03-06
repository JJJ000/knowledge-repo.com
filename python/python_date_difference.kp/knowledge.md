---
title: How to calculate the disparity between two dates using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The timedelta function calculates the difference between two dates in Python.
---

**Contents**

[TOC]

## Introduction

Calculating the difference between two dates is a common task in programming. In Python, we can use the datetime module to perform date and time operations. In this article, we will explore various ways to calculate the difference between two dates in Python.

## Method 1: Using timedelta

The timedelta class of the datetime module provides a way to represent the difference between two dates. We can create a timedelta object by subtracting one date from another. 

```python
from datetime import date, timedelta

first_date = date(2021, 6, 1)
second_date = date(2022, 6, 1)
difference = second_date - first_date

print("Difference between two dates:", difference)
```

In the above example, we create two date objects for June 1st, 2021 and June 1st, 2022. Next, we subtract the first date object from the second date object to get the difference. The output of the above code will be:

 ```
Difference between two dates: 365 days, 0:00:00
```

## Method 2: Using dateutil module

Another way to calculate the difference between two dates in Python is to use the dateutil module. This module provides a `relativedelta` class that can be used to represent the difference between two dates. 

```python
from dateutil.relativedelta import relativedelta
from datetime import date

first_date = date(2021, 6, 1)
second_date = date(2022, 6, 1)
difference = relativedelta(second_date, first_date)

print("Difference between two dates:", difference)
```

In the above example, we create two date objects for June 1st, 2021 and June 1st, 2022. Next, we create a `relativedelta` object by passing the two date objects to it. The output of the above code will be:

 ```
Difference between two dates: relativedelta(years=+1)
```

## Method 3: Using Pandas

Pandas is a popular Python library for data analysis. It provides several functions to work with dates and times. We can use the `pd.Timestamp` function to create a timestamp object from a date object and then calculate the difference between them.

```python
import pandas as pd
from datetime import date

first_date = date(2021, 6, 1)
second_date = date(2022, 6, 1)

first_timestamp = pd.Timestamp(first_date)
second_timestamp = pd.Timestamp(second_date)

difference = second_timestamp - first_timestamp

print("Difference between two dates:", difference)
```

In the above example, we create two date objects for June 1st, 2021 and June 1st, 2022. Next, we create two timestamp objects by passing them to the `pd.Timestamp` function. Finally, we subtract the first timestamp object from the second timestamp object to get the difference. The output of the above code will be:

 ```
Difference between two dates: 365 days 00:00:00
```

## Conclusion

In this article, we explored three different ways to calculate the difference between two dates in Python. The timedelta class of the datetime module, `relativedelta` class of the dateutil module, and `pd.Timestamp` function of the Pandas library can be used to calculate the difference between two dates. Depending on the requirements and the data, we can choose the appropriate method.
