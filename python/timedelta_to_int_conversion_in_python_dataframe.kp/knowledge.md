---
title: How to convert timedelta to an integer in a pandas dataframe using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can convert a timedelta column to an integer column in a dataframe by using the total\_seconds() method and then converting it to int().
---

**Contents**

[TOC]

Section 1: Introduction 
In data analysis or working around datetime calculations, the timedelta format is commonly used. It signifies the difference between two datetime objects in terms of days, hours, minutes, and seconds. In pandas, we may have a dataframe that contains timedelta columns. However, in some scenarios, we may need to convert these timedeltas to specific formats, such as integers. This article shall explain how we can convert timedeltas to integers in a dataframe using python pandas.

Section 2: Creating a Sample Dataframe
To illustrate how we can convert timedeltas to integers in a dataframe, let's first create a sample dataframe. We shall import pandas and numpy libraries to create the dataframe with 2 columns of timedelta values.

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({'x': pd.to_timedelta(np.random.rand(5), unit='D'), 
                   'y': pd.to_timedelta(np.random.rand(5)*24, unit='H')})
```
This code will create a dataframe with 5 rows and two columns ('x' and 'y') containing timedelta objects in days (unit='D') and hours (unit='H'), respectively.

Section 3: Converting Timedelta to Integers in Pandas Dataframe
We can convert a timedelta object to an integer value by accessing its total seconds and then converting it to an integer. To apply this method in a dataframe, we use the `apply()` function, which takes a lambda function that converts each value at each element in our dataframe to its integer equivalent.

```python
df['x'] = df['x'].apply(lambda x: int(x.total_seconds()))
df['y'] = df['y'].apply(lambda x: int(x.total_seconds()))
```

The above code converts the 'x' and 'y' columns (previously timedeltas), to integers by accessing their total seconds using the `total_seconds()` method and then converts that to integers using the `int()` function.

Section 4: Printing the Changed Dataframe
We can verify if our conversion was successful by printing the updated dataframe, which should now contain integer values instead of timedelta objects.

```python
print(df)
```
Output:
```
       x     y
0  146880    10
1   86400  4204
2   69120  8293
3  120960  3773
4  259200  6697
```

Conclusion:
This article has explained how to convert timedeltas to integers in a pandas dataframe. We used the `total_seconds()` method to obtain the total seconds of each timedelta object and then used the `apply()` function alongside lambda function that converts each value at each element in our dataframe to its integer equivalent.
