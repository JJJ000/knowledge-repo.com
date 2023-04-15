---
title: Transform unix timestamp to a readable date format within a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Call the `to\_datetime()` function on the unix time column of the pandas dataframe and specify the unit parameter as `s`.
---

**Contents**

[TOC]

## Section 1: Overview and Background

When working with time series data, one common data format that you may encounter is Unix time. Unix time is a system for describing a point in time, based on the number of seconds that have elapsed since January 1, 1970 at 00:00:00 UTC. While Unix time is a common format for storing time data, it is not particularly easy to read or interpret. In this tutorial, we will learn how to convert Unix time to a readable date format in a Pandas dataframe in Python.

## Section 2: Converting Unix Time to Datetime in Pandas

In order to convert Unix time to a datetime format in Pandas, we can use the `pd.to_datetime()` function. For example, suppose we have a dataframe `df` with a column `unix_time` that contains Unix timestamps. We can convert this to a datetime column using the following code:

``` python
df['datetime'] = pd.to_datetime(df['unix_time'], unit='s')

```

This will create a new column in the dataframe called `datetime`, which contains the converted datetime values.

## Section 3: Formatting Datetime in Pandas

Once we have converted the Unix time to a datetime format, we can then format the datetime values in a variety of ways. For example, we might want to display the date in a specific format, like `YYYY-MM-DD`, or we might want to include the time as well. We can use the `strftime()` function to format the datetime in a specific way. 

``` python
df['datetime_formatted'] = df['datetime'].apply(lambda x: x.strftime('%Y-%m-%d %H:%M:%S'))
```

This will add a new column to the dataframe called `datetime_formatted`, which contains the formatted datetime values.


## Section 4: Conclusion

In this tutorial, we have covered how to convert Unix time to a readable date format in a Pandas dataframe in Python. We used the `pd.to_datetime()` function to convert Unix timestamps to datetime values, and then the `strftime()` function to format the datetime values in a specific way. With this knowledge, you can now convert and format datetime values in your own Pandas dataframes.
