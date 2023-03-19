---
title: Determine the hour and minute time difference between two pandas columns
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: One possible solution is to subtract the two columns and then use the total\_seconds() method and floor division by 3600 to get the hours and modulo 60 to get the remaining minutes.
---

**Contents**

[TOC]

## Introduction:

In this tutorial, we will learn how to calculate the time difference between two pandas columns in hours and minutes in Python. We will use the pandas library to perform this operation. 

## Converting Columns to Datetime Object:

Before calculating the time difference, we need to convert the columns to a datetime object. We can do this using the `pd.to_datetime()` method. Assuming we have two columns `start_time` and `end_time`, we can convert them to a datetime object using the following code:

```python
df['start_time'] = pd.to_datetime(df['start_time'])
df['end_time'] = pd.to_datetime(df['end_time'])
```

## Calculating Time Difference:

Once we have the columns in the datetime format, we can subtract them to get the time difference. We can use the `dt.total_seconds()` method to get the time difference in seconds. We can then convert the seconds to hours and minutes using simple division and modulus operations. Here's the code:

```python
df['time_diff_seconds'] = (df['end_time'] - df['start_time']).dt.total_seconds()
df['time_diff_hours'] = df['time_diff_seconds'] // 3600
df['time_diff_minutes'] = (df['time_diff_seconds'] % 3600) // 60
```

## Conclusion:

In this tutorial, we learned how to calculate the time difference between two pandas columns in hours and minutes in Python. We used the `pd.to_datetime()` method to convert the columns to a datetime object, and the `dt.total_seconds()` method to get the time difference in seconds. We then converted the seconds to hours and minutes using simple division and modulus operations.
