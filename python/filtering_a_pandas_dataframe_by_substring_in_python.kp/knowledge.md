---
title: Search a pandas dataframe using a substring
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DataFrame.loc method to filter the DataFrame by passing a boolean condition based on the desired substring.
---

**Contents**

[TOC]

**Section 1: Overview**

Pandas DataFrame is a powerful data structure in Python for representing and manipulating tabular data. It provides various ways to filter a DataFrame by substring criteria, such as using the .str.contains() method or the .filter() method. 

**Section 2: .str.contains() Method**

The .str.contains() method can be used to filter a DataFrame by substring criteria. This method takes a string as an argument and returns a boolean value of True or False depending on whether the string is present in the DataFrame. For example, if we have a DataFrame with a column called 'Name', we can filter the DataFrame by substring criteria using the following syntax: 

`df[df['Name'].str.contains('substring')]`

This will return a DataFrame containing only rows where the 'Name' column contains the substring specified in the argument. 

**Section 3: .filter() Method**

The .filter() method can also be used to filter a DataFrame by substring criteria. This method takes a string as an argument and returns a DataFrame containing only rows where the specified string is present in the DataFrame. For example, if we have a DataFrame with a column called 'Name', we can filter the DataFrame by substring criteria using the following syntax: 

`df.filter(like='substring')`

This will return a DataFrame containing only rows where the 'Name' column contains the substring specified in the argument.

**Section 4: Conclusion**

In conclusion, pandas DataFrame can be filtered by substring criteria using either the .str.contains() method or the .filter() method. Both methods take a string as an argument and return a DataFrame containing only rows where the specified string is present in the DataFrame.
