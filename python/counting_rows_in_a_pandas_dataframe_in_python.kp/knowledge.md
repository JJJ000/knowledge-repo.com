---
title: What is the number of rows in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get the row count of a Pandas DataFrame in Python by using the DataFrame`s shape attribute.
---

**Contents**

[TOC]

**Option 1 - Using the Shape Attribute** 

The `shape` attribute of a Pandas DataFrame returns a tuple containing the number of rows and columns. To get the row count of a DataFrame, we can access the first element of the tuple, which is the row count.

```python
# Get the row count of a DataFrame
row_count = df.shape[0]
```

**Option 2 - Using the Len Function** 

The `len` function returns the number of elements in a container. We can use it to get the row count of a DataFrame by passing it the DataFrame as an argument.

```python
# Get the row count of a DataFrame
row_count = len(df)
```

**Option 3 - Using the Count Function**

The `count` function returns the number of non-NA/null observations for each column in a DataFrame. We can use it to get the row count of a DataFrame by passing it the index of the DataFrame.

```python
# Get the row count of a DataFrame
row_count = df.index.count()
```

**Option 4 - Using the Size Attribute**

The `size` attribute of a Pandas DataFrame returns the total number of elements in the DataFrame. We can use it to get the row count of a DataFrame by dividing it by the number of columns in the DataFrame.

```python
# Get the row count of a DataFrame
row_count = df.size // df.shape[1]
```
