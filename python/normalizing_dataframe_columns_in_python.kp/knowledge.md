---
title: Change the values of the columns in a dataframe so that they are all on the same scale
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the pandas.DataFrame.apply() method to apply a function to each column that normalizes the data.
---

**Contents**

[TOC]

**1. Import Libraries**

```python
import pandas as pd
```

**2. Load Data**

```python
df = pd.read_csv('data.csv')
```

**3. Normalize Data**

```python
df_norm = (df - df.mean()) / df.std()
```

**4. View Data**

```python
df_norm.head()
```
