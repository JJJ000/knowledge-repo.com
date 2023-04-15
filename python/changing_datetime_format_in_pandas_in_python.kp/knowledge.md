---
title: How can the datetime format be modified in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the .strftime() method and specify the desired datetime format as a string within the parentheses.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is a popular library for data manipulation and analysis in Python. It provides powerful tools to work with structured data, including time series data. Pandas has built-in support for datetime data types and provides certain APIs to manipulate datetime data. However, a common task is to change the datetime format in Pandas data frame. In this tutorial, we'll walk through how to do that.

Section 2: Getting the input data
For the purpose of this tutorial, let's assume that we have a Pandas data frame with a column containing datetime data in a certain format. We'll use the following code to create such a data frame:

``` python
import pandas as pd

data = {'datetime': ['2021-01-01 12:30:00', '2021-02-01 05:45:00', '2021-03-01 23:15:00']}
df = pd.DataFrame(data)
print(df)
```

This will output the following data frame:

```
             datetime
0  2021-01-01 12:30:00
1  2021-02-01 05:45:00
2  2021-03-01 23:15:00
```

Section 3: Changing the datetime format
Now, let's say we want to change the datetime format to a different one. We can achieve this using the `to_datetime()` method of Pandas, which converts a string to datetime format. We'll then use the `strftime()` method to format the datetime object as a string in the desired format. Here is the code:

``` python
df['datetime'] = pd.to_datetime(df['datetime'])
df['datetime'] = df['datetime'].dt.strftime('%Y/%m/%d %H:%M:%S')
print(df)
```

This code will convert the datetime string to a datetime object and then format it as 'YYYY/MM/DD HH:MM:SS'. The output will be as follows:

```
              datetime
0  2021/01/01 12:30:00
1  2021/02/01 05:45:00
2  2021/03/01 23:15:00
```

Section 4: Conclusion
In this tutorial, we learned how to change the datetime format in a Pandas data frame. We used the `to_datetime()` method to convert the datetime string to a datetime object and then used the `strftime()` method to format the datetime object as a string in the desired format. With this knowledge, you can easily change the datetime format in any Pandas data frame.
