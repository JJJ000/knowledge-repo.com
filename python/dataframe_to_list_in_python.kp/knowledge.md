---
title: Convert a column of a pandas dataframe into a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To convert a Pandas DataFrame column to a list in Python, use the `.tolist()` method on the column.
---

**Contents**

[TOC]

## Section 1: Introduction
The pandas library is a commonly used data analysis tool in Python. One of its most popular data structures is the DataFrame, which is essentially a table of data with rows and columns that can be manipulated using various methods in pandas.

In this tutorial, we will focus on how to convert a DataFrame column to a list in Python.

## Section 2: Converting a DataFrame column to a list using the tolist() method
One way to convert a DataFrame column to a list is by using the tolist() method. This method is straightforward and efficient.

Here's an example code snippet:

``` python
import pandas as pd

# Create a dictionary of data
data = {'Name': ['John', 'Sophia', 'Alex', 'Alice'],
        'Age': [32, 33, 25, 45],
        'City': ['San Francisco', 'New York', 'Seattle', 'Los Angeles']}

# Create a DataFrame
df = pd.DataFrame(data)

# Convert a DataFrame column to a list
names_list = df['Name'].tolist()

print(names_list)
```

This will output:

```
['John', 'Sophia', 'Alex', 'Alice']
```

## Section 3: Converting a DataFrame column to a list using the values attribute
Another way to convert a DataFrame column to a list is by using the values attribute. This approach is less efficient compared to the tolist() method, but it can be useful in certain scenarios.

Here's an example code snippet:

``` python
import pandas as pd

# Create a dictionary of data
data = {'Name': ['John', 'Sophia', 'Alex', 'Alice'],
        'Age': [32, 33, 25, 45],
        'City': ['San Francisco', 'New York', 'Seattle', 'Los Angeles']}

# Create a DataFrame
df = pd.DataFrame(data)

# Convert a DataFrame column to a list using the values attribute
names_list = df['Name'].values.tolist()

print(names_list)
```

This will output:

```
['John', 'Sophia', 'Alex', 'Alice']
```

## Section 4: Conclusion
In this tutorial, we discussed two ways to convert a DataFrame column to a list in Python using the pandas library. The tolist() method is the most efficient way, but the values attribute can also be used in certain scenarios.
