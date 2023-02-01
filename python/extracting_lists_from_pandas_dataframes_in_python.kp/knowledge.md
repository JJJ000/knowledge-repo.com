---
title: How can I obtain a list from a pandas dataframe column or row?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can get a list from a pandas dataframe column or row using the tolist() method.
---

**Contents**

[TOC]

#### Using `.tolist()`

The `.tolist()` method can be used to convert a column or row in a pandas dataframe to a list. 

```python
# Create a dataframe
import pandas as pd
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Convert column 'A' to a list
col_list = df['A'].tolist()

# Convert row 0 to a list
row_list = df.iloc[0].tolist()
```

#### Using `list()`

The `list()` function can also be used to convert a column or row in a pandas dataframe to a list. 

```python
# Create a dataframe
import pandas as pd
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Convert column 'A' to a list
col_list = list(df['A'])

# Convert row 0 to a list
row_list = list(df.iloc[0])
```

#### Using `.values`

The `.values` attribute can also be used to convert a column or row in a pandas dataframe to a list. 

```python
# Create a dataframe
import pandas as pd
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Convert column 'A' to a list
col_list = df['A'].values.tolist()

# Convert row 0 to a list
row_list = df.iloc[0].values.tolist()
```
