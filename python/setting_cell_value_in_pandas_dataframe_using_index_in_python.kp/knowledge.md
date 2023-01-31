---
title: Assign a value to a specific cell in a pandas dataframe using its index
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: df.loc[index,column] = value
---

**Contents**

[TOC]

### Section 1: Setting Value for a Particular Cell

We can set the value for a particular cell in a pandas DataFrame using the `.loc` method. The `.loc` method takes two arguments: the row index and the column index. For example, if we wanted to set the value of the cell in row 2, column 3 to 10, we would do the following:

```python
df.loc[2,3] = 10
```

### Section 2: Using Indexes

We can also use indexes to set a particular cell's value. For example, if we wanted to set the value of the cell in row 2, column "Name" to "John", we could do the following:

```python
df.loc[2, "Name"] = "John"
```

### Section 3: Setting Values for Multiple Cells

We can also set values for multiple cells in a pandas DataFrame using the `.loc` method. For example, if we wanted to set the values of the cells in rows 2, 3, and 4, columns "Name" and "Age" to "John", "Jane", and "Bob" and 20, 25, and 30 respectively, we could do the following:

```python
df.loc[[2,3,4], ["Name", "Age"]] = ["John", "Jane", "Bob", 20, 25, 30]
```

### Section 4: Setting Values for All Cells

We can also set the values for all cells in a pandas DataFrame using the `.loc` method. For example, if we wanted to set the values of all cells in the "Name" column to "John", we could do the following:

```python
df.loc[:, "Name"] = "John"
```
