---
title: Reorder the columns in a pandas table and place a specific column with its given name at the beginning
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: df = df[[desired\_column\_name] + [col for col in df.columns if col != desired\_column\_name]]
---

**Contents**

[TOC]

Section 1: Importing Pandas and Reading Data
```python
import pandas as pd

# Read data into a pandas dataframe
df = pd.read_csv('file.csv')
```
This section imports the pandas library and reads data from a CSV file into a pandas dataframe. Replace "file.csv" with the name of your CSV file.

Section 2: Move Column to Front by Name
```python
# Replace "column_name" with the name of the column you wish to move
column_name = "column_name"

# Get a list of column names
cols = df.columns.tolist()

# Move the specified column to the beginning of the list
cols.insert(0, cols.pop(cols.index(column_name)))

# Use the updated list of column names to reorder the columns
df = df.reindex(columns=cols)
```
This section moves a specified column to the front of the dataframe by name. Replace "column_name" with the name of the column you wish to move.

Section 3: Display Updated Dataframe
```python
print(df.head())
```
This section displays the updated dataframe with the specified column at the front. Replace "head()" with any other method you wish to use to display the dataframe.

Full code:
```python
import pandas as pd

# Read data into a pandas dataframe
df = pd.read_csv('file.csv')

# Replace "column_name" with the name of the column you wish to move
column_name = "column_name"

# Get a list of column names
cols = df.columns.tolist()

# Move the specified column to the beginning of the list
cols.insert(0, cols.pop(cols.index(column_name)))

# Use the updated list of column names to reorder the columns
df = df.reindex(columns=cols)

# Display the updated dataframe
print(df.head())
```
This code imports pandas, reads data from a CSV file, moves a specified column to the front of the dataframe by name, and displays the updated dataframe. Replace "file.csv" with the name of your CSV file and "column_name" with the name of the column you wish to move.
