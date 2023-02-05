---
title: Find the index of a column in a pandas dataframe using its name
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the DataFrame.columns.get\_loc() method to get the column index from a column name in a pandas DataFrame.
---

**Contents**

[TOC]

# Section 1: Get Column Index from Column Name

Pandas provides a function called `.columns.get_loc()` to get the column index from a column name. This function takes the name of the column as an argument and returns the index of the column.

# Section 2: Syntax

The syntax for `.columns.get_loc()` is as follows:

`dataframe.columns.get_loc(column_name)`

# Section 3: Example

Let's consider a dataframe named `df` with the following columns:

| Name | Age | Gender |
|------|-----|--------|
| John | 32  | Male   |
| Jane | 28  | Female |

To get the column index of the `Gender` column, we can use the following code:

`df.columns.get_loc("Gender")`

The output of this code will be `2`, which is the index of the `Gender` column.

# Section 4: Conclusion

In conclusion, the `.columns.get_loc()` function can be used to get the column index from a column name in a pandas dataframe.
