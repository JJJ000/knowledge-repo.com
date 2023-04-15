---
title: A dataframe contains strings, however, their data type is classified as "object"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, string values in a DataFrame are represented as objects in the dtype.
---

**Contents**

[TOC]

Section 1: Introduction 
In Python, Pandas library provides DataFrame as one of its core data structures to store and manipulate data in a two-dimensional tabular structure. It is similar to that of a spreadsheet, where the data is arranged in rows and columns. One of the data types that can be stored in a Pandas DataFrame is a string. However, when we access a string column of a DataFrame, we often find that the data type is shown as 'object' instead of 'string'. This can be a bit confusing to newcomers to Python, and this article aims to explain why it happens and how to interpret it. 

Section 2: Explanation of Dtype Object 
In Pandas, 'object' type refers to any non-numerical data types that can be stored in a Pandas DataFrame. This includes strings, lists, tuples, and dictionaries, along with other types of data. Therefore, even if a column of a DataFrame contains only strings, it is still stored as an object datatype, and the string datatype is considered a subtype of object. The reason for using 'object' as the primary datatype in Pandas is to allow for heterogeneous data types to be present in a single DataFrame. 

Section 3: Operations on Object DataTypes 
Since strings are stored as object datatype in DataFrames, any operations that we perform on object datatypes can be performed on string datatypes as well. For example, we can use the apply() method to apply a function to each element of a string column, just as we would with a column containing any other datatype. However, it is important to note that some of the string-specific operations provided by Python's string class, such as .upper(), .lower(), or slicing can be used directly only with the existing strings in a DataFrame column, and not with the column itself. This is because some of these methods have not been implemented in the Pandas library for object datatypes. For such operations, we need to use the pandas.Series.str accessor provided by Pandas to apply them. 

Section 4: Conclusion 
In summary, a column of a Pandas DataFrame that contains strings is stored as an object datatype to allow for different datatypes to be present in the same DataFrame. Though it may seem odd, this practice facilitates the use of functions and operations on the column. When using string-specific operations, one needs to use the Pandas.Series.str accessor.
