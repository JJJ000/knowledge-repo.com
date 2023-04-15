---
title: Use pandas to merge the columns containing dates and times
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `pd.to\_datetime()` function in pandas to combine the Date and Time columns into one datetime column.
---

**Contents**

[TOC]

## Introduction
Pandas is a popular data manipulation tool for Python that provides a rich set of features to work with structured data. In this tutorial, we will focus on how to combine date and time columns in pandas. We will use pandas datetime module to perform this operation.

### Working with datetime module

Pandas provides a built-in datetime module that can handle various datetime formats. It includes functions to parse datetime strings, create datetime objects, and perform various datetime calculations. We can access the `datetime` module by importing pandas as follows:

```python
    import pandas as pd
    from datetime import datetime, time
```

### Loading the data

We are going to use a sample data set to demonstrate how to combine date and time columns using pandas. The data set contains two columns, Date and Time.

```python
    # sample data
    df = pd.DataFrame({
        'Date': ['2021-01-01', '2021-01-02', '2021-01-03', '2021-01-04', '2021-01-05'],
        'Time': ['10:15:30', '11:30:15', '12:45:00', '14:00:00', '15:15:15']
    })
```

```python
      Date      Time
0  2021-01-01  10:15:30
1  2021-01-02  11:30:15
2  2021-01-03  12:45:00
3  2021-01-04  14:00:00
4  2021-01-05  15:15:15
```

## Using pandas to combine date and time columns

### Method 1: Using the `pd.to_datetime` function

Pandas `to_datetime()` function can be used to convert date and time columns into a single datetime object. 

```python
    df['Datetime'] = pd.to_datetime(df['Date'] + ' ' + df['Time'])
```

```python
      Date      Time            Datetime
0  2021-01-01  10:15:30 2021-01-01 10:15:30
1  2021-01-02  11:30:15 2021-01-02 11:30:15
2  2021-01-03  12:45:00 2021-01-03 12:45:00
3  2021-01-04  14:00:00 2021-01-04 14:00:00
4  2021-01-05  15:15:15 2021-01-05 15:15:15
```

### Method 2: Using the `pd.datetime.combine` function

The `pd.datetime.combine` function in pandas allows you to combine date and time columns into a single datetime object.

```python
    df['Datetime'] = [datetime.combine(datetime.strptime(row['Date'], '%Y-%m-%d').date(), datetime.strptime(row['Time'], '%H:%M:%S').time()) for index, row in df.iterrows()]
```

```python
      Date      Time            Datetime
0  2021-01-01  10:15:30 2021-01-01 10:15:30
1  2021-01-02  11:30:15 2021-01-02 11:30:15
2  2021-01-03  12:45:00 2021-01-03 12:45:00
3  2021-01-04  14:00:00 2021-01-04 14:00:00
4  2021-01-05  15:15:15 2021-01-05 15:15:15
```

## Conclusion

We have seen how to combine Date and Time columns using pandas. We can use any of the methods mentioned above depending on the preference and requirements. With Pandas powerful date-time functionality, we can handle date and time related data efficiently.
