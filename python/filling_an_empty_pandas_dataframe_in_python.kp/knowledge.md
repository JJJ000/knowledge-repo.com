---
title: Constructing a pandas dataframe from scratch and then populating it with data
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Create an empty DataFrame by passing an empty dictionary to the DataFrame constructor, then fill it by assigning values to its columns and rows.
---

**Contents**

[TOC]

**Section 1: Create an Empty DataFrame**

Pandas DataFrames can be created in a variety of ways. The simplest way to create an empty DataFrame is to use the pandas.DataFrame() constructor. This constructor takes a dictionary, list, or array as its argument and creates a DataFrame with the specified data.

```python
import pandas as pd

df = pd.DataFrame()
```

**Section 2: Add Data to DataFrame**

Once the empty DataFrame has been created, data can be added to it in several ways. The most common way is to use the .loc[] method to assign values to specific rows and columns.

For example, to add a column of values to the DataFrame, the following code can be used:

```python
df.loc[:, 'column_name'] = [1, 2, 3]
```

This code will add a column called 'column_name' to the DataFrame, with the values 1, 2, and 3.

**Section 3: Add Columns to DataFrame**

Columns can also be added to the DataFrame using the .assign() method. This method takes a dictionary as its argument, where the keys are the column names and the values are the data to be added to the columns.

For example, to add two columns to the DataFrame, the following code can be used:

```python
df = df.assign(column_1 = [4, 5, 6], column_2 = [7, 8, 9])
```

This code will add two columns to the DataFrame, 'column_1' and 'column_2', with the values 4, 5, 6 and 7, 8, 9, respectively.

**Section 4: View DataFrame**

Once the DataFrame has been filled with data, it can be viewed using the .head() method. This method takes an optional integer argument, which specifies the number of rows to be displayed. By default, the .head() method will display the first five rows of the DataFrame.

For example, to view the first three rows of the DataFrame, the following code can be used:

```python
df.head(3)
```

This code will display the first three rows of the DataFrame.
