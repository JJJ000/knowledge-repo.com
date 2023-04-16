---
title: How to remove infinite values from dataframes in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas provides the ability to drop infinite values from a dataframe using the DataFrame.dropna() function.
---

**Contents**

[TOC]

**Section 1: Overview**

Dropping infinite values from dataframes in pandas is a common task in data analysis. Pandas provides a number of methods to identify and remove infinite values from dataframes. These methods include using the isnull() and isinf() functions, as well as the dropna() and drop_duplicates() methods.

**Section 2: Using isnull() and isinf()**

The isnull() and isinf() functions can be used to identify infinite values in a dataframe. The isnull() function returns a boolean value indicating whether a value is null or not. The isinf() function returns a boolean value indicating whether a value is infinite or not. Both of these functions can be used to identify infinite values in a dataframe.

**Section 3: Using dropna() and drop_duplicates()**

The dropna() and drop_duplicates() methods can be used to remove infinite values from a dataframe. The dropna() method removes all rows with null or missing values, while the drop_duplicates() method removes all rows that contain duplicate values. Both of these methods can be used to remove infinite values from a dataframe.

**Section 4: Conclusion**

Dropping infinite values from dataframes in pandas is a common task in data analysis. Pandas provides a number of methods to identify and remove infinite values from dataframes, including using the isnull() and isinf() functions, as well as the dropna() and drop_duplicates() methods. Using these methods, data analysts can easily remove infinite values from their dataframes.
