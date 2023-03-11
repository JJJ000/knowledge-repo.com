---
title: How can you verify the data type of all the columns in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the `dtypes` attribute of the DataFrame to check the data type for all columns.
---

**Contents**

[TOC]

## Section 1: Importing the necessary libraries and creating a sample dataset

To check the dtype for all columns in a dataframe in Python, we first need to import the necessary libraries and create a sample dataset. For this purpose, we can use the pandas library to create a dataframe with columns having different datatypes.

```python
import pandas as pd

# Creating a sample dataframe
df = pd.DataFrame({
    'Name': ['John', 'Jane', 'Mike', 'Jessica'],
    'Age': [25, 30, 45, 32],
    'Income': [50000.0, 75000.0, 100000.0, 60000.0],
    'Gender': ['Male', 'Female', 'Male', 'Female'],
    'Married': [True, True, False, True]
})
```

Here, we have created a dataframe with columns having the following datatypes:
- Name: object (string)
- Age: int64 (integer)
- Income: float64 (floating-point)
- Gender: object (string)
- Married: bool (boolean)


## Section 2: Using the dtypes attribute to check the dtype for all columns

The easiest way to check the dtype for all columns in a dataframe is to use the `dtypes` attribute. This will return a pandas series with the datatypes of all columns.

```python
# Checking the dtype for all columns using dtypes
print(df.dtypes)
```

Output:
```
Name        object
Age          int64
Income     float64
Gender      object
Married       bool
dtype: object
```

As we can see, the output shows the dtype for all columns.


## Section 3: Using the select_dtypes method to select columns based on dtype

If we want to select columns based on their dtype, we can use the `select_dtypes` method. This method takes a parameter `include` or `exclude` to specify the datatypes we want to include or exclude, respectively.

```python
# Selecting columns based on dtype using select_dtypes
numeric_cols = df.select_dtypes(include=['int64', 'float64'])
print(numeric_cols)
```

Output:
```
   Age    Income
0   25   50000.0
1   30   75000.0
2   45  100000.0
3   32   60000.0
```

Here, we have selected only the columns with numeric datatypes (int64 and float64).


## Section 4: Using the info method to view column information

Another way to view the dtype for all columns is to use the `info` method. This method provides information about the dataframe, including the number of non-null values and the dtype for each column.

```python
# Viewing column information using info
df.info()
```

Output:
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 4 entries, 0 to 3
Data columns (total 5 columns):
 #   Column   Non-Null Count  Dtype  
---  ------   --------------  -----  
 0   Name     4 non-null      object 
 1   Age      4 non-null      int64  
 2   Income   4 non-null      float64
 3   Gender   4 non-null      object 
 4   Married  4 non-null      bool   
dtypes: bool(1), float64(1), int64(1), object(2)
memory usage: 292.0+ bytes
```

Here, we can see the dtype for each column in the `dtypes` row (object, int64, float64, bool).
