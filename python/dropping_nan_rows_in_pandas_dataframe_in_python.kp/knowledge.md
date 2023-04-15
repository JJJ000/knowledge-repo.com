---
title: What is the best way to remove rows from a pandas dataframe that contain a nan value in a certain column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the DataFrame.dropna() method with the subset parameter set to the column name.
---

**Contents**

[TOC]

### 1. Import Libraries

```python
import pandas as pd
```

### 2. Create a DataFrame

```python
data = {'Name': ['John', 'Paul', 'George', 'Ringo', 'John'],
        'Age': [20, 21, 19, 18, None]
        }

df = pd.DataFrame(data)
```

### 3. Drop Rows with NaN Values

```python
df.dropna(subset=['Age'], inplace=True)
```

### 4. View DataFrame

```python
print(df)
```

Output:

| Name  | Age |
|-------|-----|
| John  | 20  |
| Paul  | 21  |
| George| 19  |
| Ringo | 18  |
