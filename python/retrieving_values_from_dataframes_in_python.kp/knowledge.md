---
title: What is the procedure for retrieving a value from a cell in a dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the `df.iloc[row\_index, column\_index]` method to get a value from a cell of a dataframe in Python.
---

**Contents**

[TOC]

# Section 1: Using Indexing

Indexing can be used to access a particular cell of a dataframe. To access a cell, the row and column index of the cell needs to be specified. The syntax for accessing a cell is `df.iloc[row_index, column_index]`. 

# Section 2: Example

For example, if we have a dataframe `df` with the following values:

|  | A  | B  |
|--|----|----|
| 0 | 10 | 20 |
| 1 | 30 | 40 |

We can access the value in the cell at row 0, column A by using the following code:

```
value = df.iloc[0, 0]
print(value)
```

The output of the above code will be `10`.

# Section 3: Using Column and Row Labels

If the dataframe has labels for the rows and columns, we can use the labels to access a particular cell. The syntax for accessing a cell with labels is `df.loc[row_label, column_label]`. 

# Section 4: Example

For example, if we have a dataframe `df` with the following values:

|      | A  | B  |
|------|----|----|
| Row1 | 10 | 20 |
| Row2 | 30 | 40 |

We can access the value in the cell at row `Row1`, column `A` by using the following code:

```
value = df.loc['Row1', 'A']
print(value)
```

The output of the above code will be `10`.
