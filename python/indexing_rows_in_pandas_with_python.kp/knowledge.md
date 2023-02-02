---
title: Find the indices of rows where a particular column has a specified value in Python pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the pandas.DataFrame.loc indexer to get the index of rows where a particular column matches a certain value.
---

**Contents**

[TOC]

### Section 1 - Importing Libraries

The following libraries must be imported in order to use Pandas:

```python
import pandas as pd
```

### Section 2 - Creating the DataFrame

The dataframe must be created with the data that you want to search. For example:

```python
data = {'Name': ['John', 'Paul', 'George', 'Ringo'], 
        'Age': [30, 25, 27, 24]}

df = pd.DataFrame(data)
```

### Section 3 - Finding Index of Rows

To find the index of the rows where the column matches a certain value, use the following code:

```python
index_list = df[df['Name'] == 'John'].index.tolist()
```

This will return a list of indexes where the Name column has a value of 'John'.

### Section 4 - Output

The output of the code in Section 3 will be a list of indexes, such as:

```python
[0]
```

This means that the row with the value 'John' is at index 0.
