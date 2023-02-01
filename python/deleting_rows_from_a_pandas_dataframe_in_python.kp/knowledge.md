---
title: Removing rows from a pandas dataframe based on a specific condition
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the DataFrame.drop() method to delete rows from a pandas DataFrame based on a conditional expression.
---

**Contents**

[TOC]

**Section 1: Import Libraries**

```python
import pandas as pd
```

**Section 2: Create DataFrame**

```python
data = {'name': ['John', 'Paul', 'George', 'Ringo'],
        'age': [20, 21, 19, 18],
        'state': ['CA', 'NY', 'TX', 'FL']}

df = pd.DataFrame(data)
```

**Section 3: Delete Rows**

```python
df = df[df['age'] > 20]
```

**Section 4: View DataFrame**

```python
print(df)
```

Output:

name  age state
1  Paul   21    NY
