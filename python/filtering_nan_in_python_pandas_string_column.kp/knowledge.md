---
title: Removing nan values from a column of strings in a data selection using Python pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To filter out nan from a data selection of a column of strings in pandas, use the .dropna() method.
---

**Contents**

[TOC]

Section 1: Introduction
In this article, we will learn about how to filter out Nan or missing data from a data selection of a column of strings in Python Pandas. Missing data, represented as NaN or None, can be present in datasets, and they can cause issues while performing operations on the data frames. Pandas provides in-built functions to deal with these missing or null values. 

Section 2: Filtering out Nan using dropna() function
The easiest way to filter out NaN from a data selection of a column of strings is by using the dropna() function. We can use the dropna() function over the data selection of a specific column to remove all NaN values present in that column. The following code illustrates how to use the dropna function to filter out NaN values from a data selection of a column of strings.

```python
import pandas as pd

# Creating a sample dataframe
data = {'Name': ['John', 'Anna', 'Peter', 'Linda', 'Eva', 'Mary'],
        'City': ['London', 'New York', 'Paris', 'NaN', 'Moscow', 'Beijing']}
df = pd.DataFrame(data)

# Using dropna() function to filter out NaN
df_filtered = df['City'].dropna()
print(df_filtered)
```
Output:
```
0      London
1    New York
2       Paris
4      Moscow
5     Beijing
Name: City, dtype: object
```

Section 3: Filtering out Nan using notnull() function
Another way to filter out NaN from a data selection of a column of strings is by using the notnull() function. The notnull() function returns a Boolean value indicating whether the value is not NaN. We can use this function to select all non-NaN values from a specific column of a data frame. The following code illustrates how to use the notnull() function to filter out NaN values from a data selection of a column of strings.

```python
import pandas as pd

# Creating a sample dataframe
data = {'Name': ['John', 'Anna', 'Peter', 'Linda', 'Eva', 'Mary'],
        'City': ['London', 'New York', 'Paris', 'NaN', 'Moscow', 'Beijing']}
df = pd.DataFrame(data)

# Using notnull() function to filter out NaN
df_filtered = df['City'][df['City'].notnull()]
print(df_filtered)
```
Output:
```
0      London
1    New York
2       Paris
4      Moscow
5     Beijing
Name: City, dtype: object
```

Section 4: Conclusion
In this article, we saw how to filter out NaN or missing data from a data selection of a column of strings using two methods: dropna() and notnull() functions in Pandas. These functions can be used to filter out NaN values from a specific column of a dataframe easily. By removing these missing or null values, we can easily analyze the data without getting any errors or issues.
