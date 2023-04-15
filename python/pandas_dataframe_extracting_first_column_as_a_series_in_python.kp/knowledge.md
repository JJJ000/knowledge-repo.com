---
title: What is the method to obtain the first column of a pandas dataframe as a series?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the syntax df.iloc[,0] to get the first column of a pandas DataFrame as a Series.
---

**Contents**

[TOC]

## Section 1: Import pandas library

The first step is to import the pandas library. This can be done using the `import` keyword and assigning it an alias such as `pd`, which is the convention used in the Python community.


```python
import pandas as pd
```


## Section 2: Load data into a pandas DataFrame 

After importing the pandas module, the next step is to load data into a DataFrame. There are different ways to load or create a pandas DataFrame, including, but not limited to, using a CSV file, a dictionary, a list, etc.

```python
# create an example DataFrame
df = pd.DataFrame({'Col1': [1, 2, 3], 'Col2': [4, 5, 6], 'Col3': [7, 8, 9]})
```

`print(df)` outputs:

```
   Col1  Col2  Col3
0     1     4     7
1     2     5     8
2     3     6     9
```


## Section 3: Select the first column as a Series

Once data is loaded into a pandas DataFrame, the next step is to select the first column as a Series object. This can be done using the `.iloc` or `.loc` accessor methods.

```python
# select the first column using the .iloc method
first_col = df.iloc[:, 0]

#Alternatively, you can use the .loc method as follows
#first_col = df.loc[:, 'Col1']

# verify that it is a Series object
print(type(first_col))
```

`print(type(first_col))` outputs:

```
<class 'pandas.core.series.Series'>
```

   


## Section 4 (Optional): Display the selected Series

The selected Series can be displayed using the `print()` function. For example:

```python
print(first_col)
```

`print(first_col)` outputs:

```
0    1
1    2
2    3
Name: Col1, dtype: int64
```


Alternatively, you can also display the selected Series in a tabular format using pandas' `.to_frame()` method:

```python
print(first_col.to_frame())
```

`print(first_col.to_frame())` outputs:

```
   Col1
0     1
1     2
2     3
```
