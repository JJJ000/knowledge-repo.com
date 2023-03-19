---
title: What is the method to divide a tuple column in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use Pandas` apply() method and lambda function to split the tuples and create new columns for each element.
---

**Contents**

[TOC]

# Section 1: Create a sample pandas dataframe with columns of tuples

To demonstrate how to split a column of tuples in a pandas dataframe, we first need to create a sample dataframe with such a column. 

```
import pandas as pd

data = {'name': ['John', 'Tom', 'Jane'],
        'age': [30, 25, 35],
        'address': [('New York', 'USA'), ('London', 'UK'), ('Paris', 'France')]}

df = pd.DataFrame(data)
```

Here, we have created a dictionary `data` that contains three keys: `name`, `age`, and `address`. The key `name` contains a list of names, `age` contains a list of ages, and `address` contains a list of tuples, where each tuple consists of a city and a country.

We then created a pandas dataframe `df` using the dictionary `data`.

# Section 2: Using str.split() method to split column of tuples

To split a column of tuples in a pandas dataframe, one approach is to use the `str.split()` method. This method splits a string into a list of substrings based on a specified delimiter.

```
df[['city', 'country']] = pd.DataFrame(df['address'].tolist(), index=df.index)
df = df.drop('address', axis=1)
```

Here, we first used the `tolist()` method to convert the tuple column `address` to a list of tuples. We then used the `pd.DataFrame()` constructor to create a new dataframe from the list of tuples. We specified the column names as `city` and `country` using the `columns` argument.

Finally, we used the `drop()` method to drop the original `address` column from the original dataframe `df`.

# Section 3: Using apply() method to split column of tuples

Another approach to split a column of tuples in a pandas dataframe is to use the `apply()` method. This method applies a function to each element of a pandas series.

```
df[['city', 'country']] = df['address'].apply(pd.Series)
df = df.drop('address', axis=1)
```

Here, we used the `apply()` method to apply the `pd.Series` function to each element of the `address` column. This function creates a pandas series from each tuple in the column, with each element of the series corresponding to an element in the tuple.

We then assigned the resulting dataframe to `df` and dropped the original `address` column as before.

# Section 4: Conclusion

In this guide, we have demonstrated two ways to split a column of tuples in a pandas dataframe. The first approach uses the `str.split()` method, while the second approach uses the `apply()` method with the `pd.Series` function. Both approaches result in a new dataframe with the original column of tuples split into multiple columns containing the individual elements of each tuple.
