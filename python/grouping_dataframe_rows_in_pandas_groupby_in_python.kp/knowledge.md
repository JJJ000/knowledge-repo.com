---
title: What is the process for creating a list of grouped rows in a pandas dataframe using the groupby function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the groupby.apply() method to group rows of a dataframe into a list in pandas.
---

**Contents**

[TOC]

# Section 1: Grouping Dataframe Rows

Pandas groupby is a powerful tool for grouping dataframe rows into lists. It allows you to group rows based on certain criteria, such as values in a certain column, or a combination of columns.

# Section 2: Creating the Groupby Object

To create a groupby object, you need to specify the dataframe you want to group, as well as the columns you want to use to group the rows. This can be done using the `groupby()` method, which takes a list of column names as its argument.

# Section 3: Applying the Groupby Object

Once you have created the groupby object, you can apply it to the dataframe to group the rows into lists. This can be done using the `apply()` method, which takes a function as its argument. The function should take the groupby object as its argument, and return a list of the grouped rows.

# Section 4: Conclusion

Grouping dataframe rows into lists using pandas groupby is a powerful and efficient way to organize data. It allows you to quickly group rows based on certain criteria, and apply a function to the grouped rows to return a list of the grouped rows.
