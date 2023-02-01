---
title: Retrieving a single row of a pandas series/dataframe using its integer index
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the .iloc indexer to select a row by integer index.
---

**Contents**

[TOC]

**Section 1: Overview**

Selecting a row of a pandas series or dataframe by integer index in Python is a simple process. The row can be selected using the .iloc method, which takes an integer index as an argument. This method will return the row of the dataframe or series at the specified index. 

**Section 2: Syntax**

The syntax for selecting a row of a pandas series or dataframe by integer index is as follows:

`dataframe.iloc[index]`

Where dataframe is the name of the dataframe or series, and index is the integer index of the row to be selected.

**Section 3: Example**

For example, given a dataframe named df with the following data:

|  Name  | Age  |
|:------:|:----:|
|  John  |  20  |
|  Jane  |  22  |
|  Jack  |  24  |

The row at index 1 can be selected with the following command:

`df.iloc[1]`

This command will return the following output:

|  Name  | Age  |
|:------:|:----:|
|  Jane  |  22  |

**Section 4: Conclusion**

In conclusion, selecting a row of a pandas series or dataframe by integer index in Python is a straightforward process. The row can be selected using the .iloc method, which takes an integer index as an argument. This method will return the row of the dataframe or series at the specified index.
