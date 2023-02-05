---
title: Creating a new dataframe containing only the chosen columns as a copy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the pandas DataFrame.loc() method to select specific columns and assign them to a new DataFrame as a copy.
---

**Contents**

[TOC]

**Section 1: Importing Libraries**

```python
import pandas as pd
```

**Section 2: Creating the DataFrame**

```python
data = {'name': ['John', 'Jane', 'Jack', 'Jill'],
        'age': [20, 21, 22, 23],
        'gender': ['M', 'F', 'M', 'F'],
        'height': [180, 165, 175, 160]}

df = pd.DataFrame(data)
```

**Section 3: Extracting Columns**

```python
# Extracting columns 'name' and 'age'
selected_columns = df[['name', 'age']]

# Creating a copy of the DataFrame
selected_columns_df = selected_columns.copy()
```

**Section 4: Viewing the DataFrame**

```python
selected_columns_df
```

|    | name | age |
|---:|:-----|----:|
|  0 | John |  20 |
|  1 | Jane |  21 |
|  2 | Jack |  22 |
|  3 | Jill |  23 |
