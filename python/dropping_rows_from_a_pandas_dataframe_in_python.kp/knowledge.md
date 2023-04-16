---
title: What is the best way to remove multiple rows from a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DataFrame.drop() method to drop a list of rows from a Pandas dataframe.
---

**Contents**

[TOC]

# Section 1: Selecting Rows to Drop

The first step in dropping a list of rows from a Pandas dataframe is to select the rows you want to drop. This can be done by creating a list of the row indices that you want to drop.

# Section 2: Dropping Rows

Once you have your list of row indices, you can use the `drop()` method to drop the rows from the dataframe. The syntax for using the `drop()` method is as follows:

`df.drop(list_of_row_indices, inplace=True)`

The `inplace` argument is optional and is used to specify whether the changes should be made in place (i.e. without creating a new dataframe).

# Section 3: Verifying Rows are Dropped

To verify that the rows have been dropped from the dataframe, you can use the `info()` method to get a summary of the dataframe. This will show the number of rows that have been dropped.

# Section 4: Reindexing the Dataframe

Finally, after dropping the rows, you may want to reindex the dataframe. This can be done using the `reset_index()` method. The syntax for using this method is as follows:

`df.reset_index(inplace=True)`

The `inplace` argument is optional and is used to specify whether the changes should be made in place (i.e. without creating a new dataframe).
