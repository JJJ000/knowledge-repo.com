---
title: What is the method to locate numeric columns in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can use the select\_dtypes() method with the parameter include=`number` to find numeric columns in Pandas in Python.
---

**Contents**

[TOC]

## 1. Loading the data as a Pandas DataFrame 

To find the numeric columns in a dataset using Pandas, you first need to load the data as a Pandas DataFrame. This can be done by using the `read_csv()` function, which reads data from a CSV file and returns it as a DataFrame. You can also use other functions such as `read_excel()` for reading data from other file types.

```python
import pandas as pd

# Load the data as a Pandas DataFrame
data = pd.read_csv('data.csv')
```

In the above example, we have used `read_csv()` to load a dataset from a CSV file named `data.csv`.


## 2. Identifying the data type of each column 

Once you have loaded the dataset as a DataFrame, the next step is to identify the data type of each column. In Pandas, you can use the `dtypes` attribute of a DataFrame to get the data types of all the columns.

```python
# Get the data type of each column
data.dtypes
```

This will return a Series object with the data type of each column as its values.


## 3. Filtering numeric columns 

After identifying the data type of each column, you can filter the numeric columns using the `select_dtypes()` method of a DataFrame. This method allows you to select columns based on their data type.

```python
# Filter numeric columns
numeric_cols = data.select_dtypes(include=['float64', 'int64'])
```

In the above example, we have used `select_dtypes()` to select the columns that have a data type of `float64` or `int64`. This returns a new DataFrame containing only the numeric columns.


## 4. Printing the numeric columns 

Finally, you can print the names of the numeric columns using the `columns` attribute of the resulting DataFrame.

```python
# Print the names of the numeric columns
print(numeric_cols.columns)
```

This will print the names of the columns that have been filtered as numeric.
