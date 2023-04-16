---
title: Creating a new column in a pandas series/dataframe based on a conditional statement
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas can create a new column in a DataFrame or Series using the assign() method, or by directly assigning to the new column using bracket notation.
---

**Contents**

[TOC]

**Section 1: Overview**

Pandas conditional creation of a series or dataframe column is a powerful feature that allows users to create new columns based on conditions specified by the user. This can be used to filter, modify, or create new data based on existing data in the dataframe. In this article, we will discuss how to conditionally create a series or dataframe column using Pandas in Python.

**Section 2: Creating a Series Column**

To conditionally create a series column, we must first define the dataframe and the series to be added. For example, if we have a dataframe df with two columns, 'A' and 'B', and we want to conditionally create a third column 'C' based on the values of 'A' and 'B', we can use the following code:

```
df['C'] = np.where(df['A'] > df['B'], 'A is greater', 'B is greater')
```

This code will create a new column 'C' in the dataframe df with values of 'A is greater' if A is greater than B and 'B is greater' if B is greater than A.

**Section 3: Creating a Dataframe Column**

Creating a dataframe column is similar to creating a series column, however, instead of a single value, we are creating multiple values for each row in the dataframe. For example, if we have a dataframe df with two columns, 'A' and 'B', and we want to conditionally create a third column 'C' based on the values of 'A' and 'B', we can use the following code:

```
df['C'] = df.apply(lambda row: 'A is greater' if row['A'] > row['B'] else 'B is greater', axis=1)
```

This code will create a new column 'C' in the dataframe df with values of 'A is greater' if A is greater than B and 'B is greater' if B is greater than A.

**Section 4: Conclusion**

In conclusion, Pandas conditional creation of a series or dataframe column is a powerful feature that allows users to create new columns based on conditions specified by the user. This can be used to filter, modify, or create new data based on existing data in the dataframe.
