---
title: Obtain a collection of columns in a pandas dataframe by filtering their data type
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: One way to get a list of pandas dataframe columns based on data type is to use the select\_dtypes() method.
---

**Contents**

[TOC]

## Introduction
Pandas is a Python library that is used for data manipulation and analysis. It provides a vast range of functionalities for working with tabular data. One of the key features of Pandas is a DataFrame, which is an essential two-dimensional table or spreadsheet. In this guide, we will learn how to get a list of pandas dataframe columns based on data type in Python.

## Understanding the Problem
Sometimes we need to select specific columns from a pandas dataframe based on their data type. For example, we may want to select only the integer columns or only the object columns. This can be useful when we want to perform some operations on columns with specific data types.

## Solution
Pandas provides several methods to help us get the list of dataframe columns based on data type. Let's discuss them one by one.

### Using Select_Dtypes Method
The `select_dtypes` method is a convenient way to select columns from a dataframe based on their data type. We can pass one or more data types in the `include` parameter or exclude some data types using the `exclude` parameter.

```python
import pandas as pd

df = pd.DataFrame({
    'name':['John', 'Mary', 'Peter', 'Lucy'],
    'age':[23, 45, 12, 34],
    'city':['New York', 'Paris', 'Tokyo', 'Sydney'],
    'sex':['M', 'F', 'M', 'F']
})

# select all columns with datatype 'object'
obj_cols = df.select_dtypes(include=['object']).columns.tolist()
print(obj_cols)
# Output: ['name', 'city', 'sex']

# select all columns with datatype 'int'
int_cols = df.select_dtypes(include=['int']).columns.tolist()
print(int_cols)
# Output: ['age']
```

### Using Dtypes Property
Another way to get a list of dataframe columns based on data type is to use the `dtypes` property of the DataFrame. We can filter the column names based on their datatypes using the `isin` method.

```python
import pandas as pd

df = pd.DataFrame({
    'name':['John', 'Mary', 'Peter', 'Lucy'],
    'age':[23, 45, 12, 34],
    'city':['New York', 'Paris', 'Tokyo', 'Sydney'],
    'sex':['M', 'F', 'M', 'F']
})

# get all columns with datatype 'object'
obj_cols = df.columns[df.dtypes.isin(['object'])].tolist()
print(obj_cols)
# Output: ['name', 'city', 'sex']

# get all columns with datatype 'int'
int_cols = df.columns[df.dtypes.isin(['int'])].tolist()
print(int_cols)
# Output: ['age']
```

### Using Info Method
Pandas `info()` method provides useful information about the DataFrame, including the datatype of each column. We can extract the column names based on their datatype from the output of the `info()` method.

```python
import pandas as pd

df = pd.DataFrame({
    'name':['John', 'Mary', 'Peter', 'Lucy'],
    'age':[23, 45, 12, 34],
    'city':['New York', 'Paris', 'Tokyo', 'Sydney'],
    'sex':['M', 'F', 'M', 'F']
})

# get all columns with datatype 'object'
obj_cols = [col[0] for col in df.info(verbose=False) if col[1] == 'object']
print(obj_cols)
# Output: ['name', 'city', 'sex']

# get all columns with datatype 'int'
int_cols = [col[0] for col in df.info(verbose=False) if col[1] == 'int']
print(int_cols)
# Output: ['age']
```

### Using List Comprehension
We can also use list comprehension to get a list of dataframe columns based on data type. We can loop through all columns and append the column name to a list if its datatype matches our desired datatype.

```python
import pandas as pd

df = pd.DataFrame({
    'name':['John', 'Mary', 'Peter', 'Lucy'],
    'age':[23, 45, 12, 34],
    'city':['New York', 'Paris', 'Tokyo', 'Sydney'],
    'sex':['M', 'F', 'M', 'F']
})

# get all columns with datatype 'object'
obj_cols = [col for col in df.columns if df[col].dtype == 'object']
print(obj_cols)
# Output: ['name', 'city', 'sex']

# get all columns with datatype 'int'
int_cols = [col for col in df.columns if df[col].dtype == 'int']
print(int_cols)
# Output: ['age']
```

## Conclusion
In this guide, we learned how to get a list of pandas dataframe columns based on data type in Python. We discussed four different methods to achieve this task, including `select_dtypes`, `dtypes`, `info()` method, and list comprehension.
