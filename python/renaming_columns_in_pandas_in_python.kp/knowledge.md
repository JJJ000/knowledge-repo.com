---
title: Changing the labels of columns in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Use the `DataFrame.rename()` method to rename columns in a Pandas DataFrame.
---

**Contents**

[TOC]

### Accessing Column Names

Pandas offers a variety of ways to access the column names of a given dataframe. The most straightforward way to access the column names is by using the `columns` attribute of the dataframe. This attribute returns an array of column names:

```python
df.columns  # returns array of column names
```

### Renaming Columns

Renaming columns in a dataframe can be done using the `rename` method. This method takes a dictionary of old names as keys and new names as values. 

```python
df.rename(columns={'old_name': 'new_name'}, inplace=True)
```

The `inplace` parameter is used to indicate whether the changes should be applied directly to the dataframe. If this parameter is set to `True`, the changes will be applied to the dataframe, otherwise the changes will be returned as a new dataframe.

### Renaming All Columns

If you want to rename all columns in the dataframe, you can use the `columns` attribute to create a dictionary of old and new names. The `columns` attribute returns an array of column names, which can be used to create a dictionary of old and new names:

```python
new_names = {old_name: new_name for old_name, new_name in zip(df.columns, new_column_names)}
df.rename(columns=new_names, inplace=True)
```

### Renaming Select Columns

If you want to rename only select columns, you can create a dictionary of old and new names and pass it to the `rename` method. The `rename` method will only rename the columns specified in the dictionary.

```python
select_columns = {'old_name1': 'new_name1', 'old_name2': 'new_name2'}
df.rename(columns=select_columns, inplace=True)
```
