---
title: Looping over a sequence of dates in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can iterate through a range of dates in Python by using the dateutil.rrule module.
---

**Contents**

[TOC]

**Using the Datetime Library**

The datetime library is the most straightforward way to iterate through a range of dates in Python. The library contains the `date()` and `timedelta()` functions which can be used to create a range of dates. 

The `date()` function is used to create a date object. It takes three arguments: year, month, and day. The `timedelta()` function is used to add a specified number of days to a date object.

Example:

```
from datetime import date, timedelta

# Create a date object for the start date
start_date = date(2020, 1, 1)

# Create an empty list to store the dates
dates = []

# Create a loop that adds one day to the start date
for i in range(10):
    new_date = start_date + timedelta(days=i)
    dates.append(new_date)

print(dates)
```

**Using a While Loop**

Another way to iterate through a range of dates in Python is to use a while loop. The while loop will continue to run until a specified condition is met. 

The loop can be used to increment the date by one day and add it to a list until the desired end date is reached. The loop will need to be set up to check if the current date is less than the end date, and if so, increment the date by one day and add it to the list. 

Example:

```
from datetime import date, timedelta

# Create a date object for the start date
start_date = date(2020, 1, 1)

# Create a date object for the end date
end_date = date(2020, 1, 10)

# Create an empty list to store the dates
dates = []

# Create a while loop that adds one day to the start date
while start_date <= end_date:
    dates.append(start_date)
    start_date += timedelta(days=1)

print(dates)
```

**Using a For Loop**

A third way to iterate through a range of dates in Python is to use a for loop. The for loop can be used to loop through a range of dates and add them to a list. 

The loop will need to be set up to loop through a range of dates from the start date to the end date, and add each date to the list. 

Example:

```
from datetime import date

# Create a date object for the start date
start_date = date(2020, 1, 1)

# Create a date object for the end date
end_date = date(2020, 1, 10)

# Create an empty list to store the dates
dates = []

# Create a for loop that adds one day to the start date
for i in range(int((end_date - start_date).days) + 1):
    new_date = start_date + timedelta(days=i)
    dates.append(new_date)

print(dates)
```

**Using a List Comprehension**

The fourth way to iterate through a range of dates in Python is to use a list comprehension. The list comprehension is a compact way to generate a list by performing an operation on each item in an iterable. 

The list comprehension can be used to loop through a range of dates and add them to a list. The loop will need to be set up to loop through a range of dates from the start date to the end date, and add each date to the list. 

Example:

```
from datetime import date, timedelta

# Create a date object for the start date
start_date = date(2020, 1, 1)

# Create a date object for the end date
end_date = date(2020, 1, 10)

# Create a list comprehension that adds one day to the start date
dates = [start_date + timedelta(days=x) for x in range(int((end_date - start_date).days) + 1)]

print(dates)
```
