---
title: Transform a pandas dataframe into a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas DataFrame can be converted to a dictionary using the DataFrame.to\_dict() method.
---

**Contents**

[TOC]

### Section 1: Importing Libraries

```python
import pandas as pd
```

### Section 2: Creating DataFrame

```python
data = {'Name':['Tom', 'nick', 'krish', 'jack'],
        'Age':[20, 21, 19, 18]}
 
df = pd.DataFrame(data)
```

### Section 3: Converting to Dictionary

```python
df_dict = df.to_dict('records')
```

### Section 4: Output

```python
print(df_dict)

[{'Name': 'Tom', 'Age': 20},
 {'Name': 'nick', 'Age': 21},
 {'Name': 'krish', 'Age': 19},
 {'Name': 'jack', 'Age': 18}]
```
