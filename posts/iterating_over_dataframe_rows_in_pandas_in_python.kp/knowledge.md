---
title: What is the process for looping through each row in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `iterrows()` function to iterate over rows in a DataFrame in Pandas.
---

**Contents**

[TOC]

### Using `iterrows()`
The `iterrows()` function in Pandas allows you to iterate over rows in a DataFrame. The syntax for this is:

```python
for index, row in df.iterrows():
    # do something
```

Where `df` is your DataFrame and `index` is the index of the row and `row` is the row itself.

### Example
The following example shows how to use `iterrows()` to iterate over the rows of a DataFrame and print the values of each row:

```python
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# iterate over rows
for index, row in df.iterrows():
    print(row['A'], row['B'], row['C'])

# output:
1 4 7
2 5 8
3 6 9
```

### Using `itertuples()`
Another option for iterating over rows in a DataFrame is to use the `itertuples()` function. This is similar to `iterrows()` but more efficient as it avoids the need to create a `Series` object for each row. The syntax for this is:

```python
for row in df.itertuples():
    # do something
```

Where `df` is your DataFrame and `row` is the row itself.

### Example
The following example shows how to use `itertuples()` to iterate over the rows of a DataFrame and print the values of each row:

```python
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# iterate over rows
for row in df.itertuples():
    print(row.A, row.B, row.C)

# output:
1 4 7
2 5 8
3 6 9
```
