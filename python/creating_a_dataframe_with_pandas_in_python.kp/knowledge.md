---
title: How can I add data to an empty dataframe in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can create a new DataFrame and then use the .append() method to add rows to it.
---

**Contents**

[TOC]

**Section 1: Creating an Empty DataFrame**

The first step to appending to an empty DataFrame in Pandas is to create an empty DataFrame. This can be done with the following code:

```python
import pandas as pd

df = pd.DataFrame()
```

This will create an empty DataFrame with no columns or rows. 

**Section 2: Appending Rows**

The next step is to append rows to the empty DataFrame. This can be done with the `.append()` method. For example, to append a row with the values `[1, 2, 3]` to the DataFrame `df`, the following code can be used:

```python
df = df.append([[1, 2, 3]])
```

This will append the row to the DataFrame.

**Section 3: Appending Columns**

The next step is to append columns to the empty DataFrame. This can be done with the `.assign()` method. For example, to append a column with the name `'A'` and the values `[1, 2, 3]` to the DataFrame `df`, the following code can be used:

```python
df = df.assign(A=[1, 2, 3])
```

This will append the column to the DataFrame.

**Section 4: Adding More Rows and Columns**

The same process can be used to add more rows and columns to the DataFrame. For example, to add a row with the values `[4, 5, 6]` and a column with the name `'B'` and the values `[4, 5, 6]` to the DataFrame `df`, the following code can be used:

```python
df = df.append([[4, 5, 6]]).assign(B=[4, 5, 6])
```

This will append the row and column to the DataFrame.
