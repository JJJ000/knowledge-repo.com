---
title: Delete pandas entries with repeated index numbers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can drop duplicate indices in pandas using the DataFrame.drop\_duplicates() method.
---

**Contents**

[TOC]

1. Identifying Duplicate Rows
--------------------------------

The first step in removing duplicate rows is to identify which rows are duplicates. This can be done by using the `DataFrame.duplicated()` method. This method returns a Boolean Series with a True value for each duplicated row. 

2. Removing Duplicate Rows
--------------------------------

Once the duplicate rows have been identified, they can be removed using the `DataFrame.drop_duplicates()` method. This method takes an optional `subset` argument which can be used to specify which columns to use when identifying duplicates.

3. Resetting the Index
--------------------------------

The index of the DataFrame should be reset after the duplicate rows have been removed, as the indices of the original rows will have been removed. This can be done using the `DataFrame.reset_index()` method.

4. Dropping the Old Index
--------------------------------

Finally, the old index should be dropped from the DataFrame. This can be done using the `DataFrame.drop()` method, with the argument `columns` set to `'index'`.
