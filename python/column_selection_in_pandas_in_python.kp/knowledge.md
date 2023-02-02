---
title: Filtering/omitting columns in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the Pandas DataFrame.loc or DataFrame.iloc methods to select or exclude sets of columns in a DataFrame.
---

**Contents**

[TOC]

**Selecting Columns:**

1. Using String or List of String: 
   Pandas allows you to select columns by passing a string or list of strings to the indexing operator. For example, df[‘column_name’] will select the column with the name ‘column_name’ from the DataFrame. 

2. Using .loc: 
   The .loc indexer can also be used to select columns. It allows you to select columns by label. For example, df.loc[:, ‘column_name’] will select the column with the name ‘column_name’ from the DataFrame. 

**Excluding Columns:**

1. Using String or List of String: 
   Pandas allows you to exclude columns by passing a string or list of strings to the indexing operator. For example, df[‘column_name’] will exclude the column with the name ‘column_name’ from the DataFrame. 

2. Using .loc: 
   The .loc indexer can also be used to exclude columns. It allows you to exclude columns by label. For example, df.loc[:, ‘column_name’] will exclude the column with the name ‘column_name’ from the DataFrame.
