---
title: Remove a column from a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DataFrame.drop() method to delete a column from a Pandas DataFrame.
---

**Contents**

[TOC]

### 1. Locate the Column

The first step to deleting a column from a Pandas DataFrame is to locate the column. This can be done by using the `DataFrame.columns` attribute, which returns a list of the columns in the DataFrame.

### 2. Drop the Column

Once the column has been located, it can be dropped from the DataFrame by using the `DataFrame.drop()` method. This method takes the column name as an argument and drops the column from the DataFrame.

### 3. Confirm the Column has been Dropped

Finally, the user should confirm that the column has been dropped by using the `DataFrame.columns` attribute again. This will return a list of the columns in the DataFrame without the dropped column.

### 4. Reindex the DataFrame

After dropping the column, the user should reindex the DataFrame to ensure that the index is in the correct order. This can be done using the `DataFrame.reset_index()` method.
