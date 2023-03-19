---
title: Assign the data type of the column in the pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can assign pandas dataframe column dtypes using the astype() method in Python.
---

**Contents**

[TOC]

# Introduction
A pandas DataFrame is a two-dimensional tabular data structure with columns that can have different data types. You can assign pandas DataFrame column data types to make sure that each column has the correct data type for the data it contains. Here are the steps to assign pandas DataFrame column data types in Python.

# Step 1: Import pandas
The first step is to import the pandas library into your Python code.

```python
import pandas as pd
```

# Step 2: Create a DataFrame
Next, create a pandas DataFrame with columns that need to be assigned data types.

```python
df = pd.DataFrame({'column1': [1, 2, 3, 4],
                   'column2': ['a', 'b', 'c', 'd'],
                   'column3': [1.1, 2.2, 3.3, 4.4]})
```

# Step 3: Assign data types to columns
Finally, assign pandas DataFrame column data types using the `astype()` method.

```python
df['column1'] = df['column1'].astype(int)
df['column2'] = df['column2'].astype(str)
df['column3'] = df['column3'].astype(float)
```

The `astype()` method takes the data type you want to assign as an argument. Possible data types include `int`, `float`, `str`, and others.

# Conclusion
By following these steps, you can assign pandas DataFrame column data types to make sure each column has the correct data type for the data it contains.
