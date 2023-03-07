---
title: Produce a date that is selected randomly within a range of two other dates
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To generate a randomized date between two specified dates in Python, you can use the datetime and random modules.
---

**Contents**

[TOC]

## Importing required libraries

To generate a random date between two dates in Python, we will need to use the datetime module. So, let's start by importing the required module.


```python
import datetime
```

## Defining start and end date

Now, we need to define the start and end date between which we want to generate the random date. Let's assume we want to generate a random date between 1st Jan 2020 and 31st Dec 2020. We can create objects of the datetime.date class to represent these dates.


```python
start_date = datetime.date(2020, 1, 1)
end_date = datetime.date(2020, 12, 31)
```

## Generating random date

Now, we can use the datetime.timedelta class to generate a random number of days between the start and end dates. We can then add this number of days to the start date to get the random date.


```python
random_number_of_days = (end_date - start_date).days
random_days = datetime.timedelta(days=random.randint(0, random_number_of_days))
random_date = start_date + random_days
```

The above code will generate a random date between 1st Jan 2020 and 31st Dec 2020. You can modify the start and end dates as per your requirements.
