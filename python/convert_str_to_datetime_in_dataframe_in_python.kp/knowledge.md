---
title: Change the data type of a dataframe column from string to datetime
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the pd.to\_datetime() method to convert a DataFrame column from string to datetime.
---

**Contents**

[TOC]

### Section 1: Import Libraries

```python
import pandas as pd
from datetime import datetime
```

### Section 2: Read Data

```python
# Read the data
df = pd.read_csv('data.csv')

# View the data
df.head()
```

### Section 3: Convert to Datetime

```python
# Convert the column to datetime
df['date_column'] = pd.to_datetime(df['date_column'])

# View the data
df.head()
```

### Section 4: Confirm Conversion

```python
# Confirm the conversion
df.dtypes
```
