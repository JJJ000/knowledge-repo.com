---
title: What is the procedure for determining the number of nan values in a column in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can count the NaN values in a column in a pandas DataFrame by using the df.isna().sum() command.
---

**Contents**

[TOC]

## Option 1

### Step 1:
Create a boolean mask for the column of interest:

```python
mask = df['column_name'].isnull()
```

### Step 2:
Apply the boolean mask to the column of interest and count the number of `True` values:

```python
num_nulls = df[mask]['column_name'].count()
```

## Option 2

### Step 1:
Create a series object with the number of NaN values per column:

```python
null_series = df.isnull().sum()
```

### Step 2:
Access the column of interest and count the number of NaN values:

```python
num_nulls = null_series['column_name']
```
