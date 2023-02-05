---
title: Find the row with the highest value for a column in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: df.loc[df[`column`].idxmax()]
---

**Contents**

[TOC]

**Section 1: Importing Libraries**

```python
import pandas as pd
```

**Section 2: Creating DataFrame**

```python
data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],'Age':[28,34,29,42]}
df = pd.DataFrame(data)
```

**Section 3: Finding Max Value**

```python
max_value = df['Age'].max()
```

**Section 4: Finding Row with Max Value**

```python
max_row = df[df['Age'] == max_value]
```
