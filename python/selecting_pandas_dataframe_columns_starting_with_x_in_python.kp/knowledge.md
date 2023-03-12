---
title: What is the method for choosing all the columns in a pandas dataframe that begin with the letter x?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the loc accessor with a boolean condition that checks if the column names start with `X` df.loc[, df.columns.str.startswith(`X`)].
---

**Contents**

[TOC]

## Step 1: Import the pandas library

```python
import pandas as pd
```

## Step 2: Create a DataFrame

```python
data = {
    'X1': [1, 2, 3],
    'X2': [4, 5, 6],
    'Y1': [7, 8, 9],
    'Y2': [10, 11, 12]
}
df = pd.DataFrame(data)
```

## Step 3: Select all columns whose names start with 'X'

```python
x_cols = [col for col in df.columns if col.startswith('X')]
x_df = df[x_cols]
```

The variable `x_cols` will contain a list of all column names that start with 'X'. We can then select these columns from the DataFrame by using the list `x_cols` as the column index. The resulting DataFrame is stored in the variable `x_df`.
