---
title: Generate a list of day-dates that fall within a specified date range
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use a loop to iterate over each date between the start and end dates and print the string representation of each date in the desired format.
---

**Contents**

[TOC]

## Obtaining user input

The first section of the Python program will be to obtain user input for the start and end dates. We will be using the `datetime` module to represent the dates.

```python
import datetime

start = input("Enter the start date (YYYY-MM-DD): ")
end = input("Enter the end date (YYYY-MM-DD): ")

start_date = datetime.datetime.strptime(start, '%Y-%m-%d')
end_date = datetime.datetime.strptime(end, '%Y-%m-%d')
```

Here, we are using the `strptime()` method of the `datetime` module to parse the date strings entered by the user and convert them to `datetime` objects. We are using the format `%Y-%m-%d` to specify that the date should be in Year-Month-Day format.

## Printing day-dates between the two dates

The next section of the program will be to print all the day-dates between the start and end dates. We will be using a `while` loop to iterate over the dates and print them one by one.

```python
current_date = start_date
while current_date <= end_date:
    print(current_date.strftime('%Y-%m-%d'))
    current_date += datetime.timedelta(days=1)
```

Here, we are using the `strftime()` method of the `datetime` module to format the `datetime` object as a string in the form `YYYY-MM-DD` and then printing it to the console. We are also using the `timedelta()` method of the `datetime` module to increment the current date by one day for each iteration of the loop.

## Putting it all together

The complete Python program to print all the day-dates between two dates would look like this:

```python
import datetime

start = input("Enter the start date (YYYY-MM-DD): ")
end = input("Enter the end date (YYYY-MM-DD): ")

start_date = datetime.datetime.strptime(start, '%Y-%m-%d')
end_date = datetime.datetime.strptime(end, '%Y-%m-%d')

current_date = start_date
while current_date <= end_date:
    print(current_date.strftime('%Y-%m-%d'))
    current_date += datetime.timedelta(days=1)
```

Note that this program assumes that the user will enter the dates in the format `YYYY-MM-DD`. If you want to handle other date formats, you will need to modify the `strptime()` format string accordingly.
