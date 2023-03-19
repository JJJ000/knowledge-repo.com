---
title: What is the method for examining the dtype of a column using python's pandas library?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the `.dtype` attribute after selecting a specific column to check the data type in Python Pandas.
---

**Contents**

[TOC]

## Introduction

Data types are an important aspect of data analysis in Python Pandas. Pandas provide several options to check the dtype of a column in a DataFrame. In this tutorial, we will explore some of the ways to check the dtype of a column in Python Pandas.

## Method 1: .dtypes

The simplest way to check the dtype of a column is to use the `.dtypes` attribute of a DataFrame. This attribute returns a pandas Series with the data type of each column in the DataFrame.

```python
import pandas as pd

# create a sample DataFrame
data = {'col1': [1,2,3],'col2': ['a','b','c'], 'col3': [1.23, 4.56, 7.89]}
df = pd.DataFrame(data)

# check the dtype of each column
print(df.dtypes)
```
**Output:**

```
col1      int64
col2     object
col3    float64
dtype: object
```

## Method 2: select_dtype()

The `.select_dtype()` method is used to select columns based on their dtype. We can use this method to check if a column has a specific dtype.

```python
import pandas as pd

# create a sample DataFrame
data = {'col1': [1,2,3],'col2': ['a','b','c'], 'col3': [1.23, 4.56, 7.89]}
df = pd.DataFrame(data)

# check if col1 has integer dtype
if df['col1'].select_dtype(include=['int']):
    print('col1 has integer dtype')
else:
    print('col1 does not have integer dtype')
```

**Output:**

```
col1 has integer dtype
```

## Method 3: .info()

The `.info()` method provides a summary of the DataFrame, including the dtypes of each column.

```python
import pandas as pd

# create a sample DataFrame
data = {'col1': [1,2,3],'col2': ['a','b','c'], 'col3': [1.23, 4.56, 7.89]}
df = pd.DataFrame(data)

# check the dtypes using .info()
print(df.info())
```

**Output:**

```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3 entries, 0 to 2
Data columns (total 3 columns):
 #   Column  Non-Null Count  Dtype  
---  ------  --------------  -----  
 0   col1    3 non-null      int64  
 1   col2    3 non-null      object 
 2   col3    3 non-null      float64
dtypes: float64(1), int64(1), object(1)
memory usage: 200.0+ bytes
```

## Conclusion

In this tutorial, we have explored three methods to check the dtype of a column in Python Pandas. We have learned how to use the `.dtype` attribute of a DataFrame, the `.select_dtype()` method, and the `.info()` method. These methods can be used to check the dtype of a column based on the requirements of a specific analysis.
