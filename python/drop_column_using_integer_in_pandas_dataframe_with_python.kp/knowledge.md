---
title: How can I remove a column using integer value in pandas dataframe using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To drop a column in a Pandas DataFrame using an integer index, use the `DataFrame.drop` method with the `axis` parameter set to 1 and the `columns` parameter to the integer index.
---

**Contents**

[TOC]

## Section 1: Introduction to Pandas DataFrames

Pandas is an open-source data manipulation library for Python, which provides easy-to-use data structures and data analysis tools. One of the most commonly used data structures in Pandas is the DataFrame. A Pandas DataFrame is a two-dimensional table-like data structure that consists of rows and columns, where each column can have a different data type.

## Section 2: Removing a column from a Pandas DataFrame using column name

To remove a column from a Pandas DataFrame using the column name, we can use the `drop()` method of the DataFrame object. Here's how we can do it:

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({
    'Name': ['John', 'Alice', 'Bob'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Paris', 'London']
})

# Remove the 'City' column
df = df.drop('City', axis=1)
```

In the above code, we first create a Pandas DataFrame with three columns: 'Name', 'Age', and 'City'. Then, we use the `drop()` method to remove the 'City' column from the DataFrame, and assign the resulting DataFrame back to the variable `df`. 

Note that in the `drop()` method, we need to specify the column name and the axis along which we want to drop the column. Since we want to drop a column, we set `axis=1`.

## Section 3: Removing a column from a Pandas DataFrame using column index

To remove a column from a Pandas DataFrame using the column index, we can use the `drop()` method of the DataFrame object. Here's how we can do it:

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({
    'Name': ['John', 'Alice', 'Bob'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Paris', 'London']
})

# Remove the second column (index=1)
df = df.drop(df.columns[1], axis=1)
```

In the above code, we first create a Pandas DataFrame with three columns: 'Name', 'Age', and 'City'. Then, we use the `drop()` method to remove the second column (index=1) from the DataFrame, and assign the resulting DataFrame back to the variable `df`. 

Note that in the `drop()` method, we need to specify the column index using `df.columns[1]` and the axis along which we want to drop the column using `axis=1`.

## Section 4: Conclusion

In this tutorial, we learned how to remove a column from a Pandas DataFrame using column name and column index. The `drop()` method of the DataFrame object is used for both these methods, with the `axis` parameter set to 1 to indicate that we want to drop a column. By understanding these methods, we can easily manipulate and clean up data in a Pandas DataFrame.
