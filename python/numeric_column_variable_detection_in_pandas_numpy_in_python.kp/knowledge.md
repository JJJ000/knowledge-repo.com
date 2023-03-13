---
title: What is the method to identify if a column or variable is numeric in pandas/numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The dtype attribute can be used to determine whether a column/variable is numeric or not in Pandas/NumPy in Python.
---

**Contents**

[TOC]

Checking Data Types of Columns in Pandas/NumPy

There are various ways to check whether a column/variable is numeric or not in Pandas/NumPy in Python.

1. Using the dtype attribute of the pandas DataFrame 
We can use dtype attribute to check the data types of all the columns of a pandas DataFrame. We can add the select_dtypes() method to the DataFrame and pass in 'number' data type to check all the columns with numeric values.

```python
import pandas as pd

df = pd.DataFrame({'A':[1,2,3],'B':['a','b','c'],'C':[4.0,5.0,6.0]})
print(df.select_dtypes(include='number').columns)
```

Output:
```
Index(['A', 'C'], dtype='object')
```

2. Using the numpy issubdtype() method
We can also use the numpy module to verify if a column is numeric or not. In that case, we can use the numpy issubdtype() method which tests whether the given data type belongs to the provided data type.

```python
import numpy as np
import pandas as pd

df = pd.DataFrame({'A':[1,2,3],'B':['a','b','c'],'C':[4.0,5.0,6.0]})

for column in df:
    if np.issubdtype(df[column].dtype, np.number):
        print(column, 'is numeric')
    else:
        print(column, 'is not numeric')
```

Output:
```
A is numeric
B is not numeric
C is numeric
```

3. Using the pandas to_numeric() function
We can also use the pandas to_numeric() function to try to convert all columns to numeric. This function is very useful if we have mixed data types in a single column, and we want to convert all the values to the corresponding numeric data type. We can use errors='coerce' to set all non-numeric values to NaN, and then check which columns still have non-null values.

```python
import pandas as pd

df = pd.DataFrame({'A':[1,2,3],'B':['a','b','c'],'C':[4.0,5.0,6.0]})
df = df.apply(pd.to_numeric, errors='coerce')

for column in df:
    if df[column].notnull().all():
        print(column, 'is numeric')
    else:
        print(column, 'is not numeric')
```

Output:
```
A is numeric
B is not numeric
C is numeric
```

4. Using regular expression package
We can also use the python regular expression package to check if a column contains only numeric values. This method can be useful if we have a small dataset with mixed data types, and we want to make sure that certain columns only contain numeric values.

```python
import pandas as pd
import re

df = pd.DataFrame({'A':[1,2,3],'B':['a','b','c'],'C':[4.0,5.0,6.0]})

for column in df:
    if re.match(r'^\d+\.?\d*$', str(df[column].values[0])):
        print(column, 'is numeric')
    else:
        print(column, 'is not numeric')
```

Output:
```
A is numeric
B is not numeric
C is numeric
```
