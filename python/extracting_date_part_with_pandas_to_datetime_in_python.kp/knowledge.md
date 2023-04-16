---
title: Retain only the date component when using pandas.to_datetime
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the parameter `errors=`coerce``.
---

**Contents**

[TOC]

**Section 1: Import Necessary Libraries**

```python
import pandas as pd
```

**Section 2: Create a DataFrame**

```python
# Create a dataframe with a date column
df = pd.DataFrame({'date': ['01/01/2020 12:00:00', '01/02/2020 12:00:00', '01/03/2020 12:00:00']})
```

**Section 3: Use pandas.to_datetime**

```python
# Convert the date column to datetime
df['date'] = pd.to_datetime(df['date'])
```

**Section 4: Keep Only Date Part**

```python
# Keep only the date part
df['date'] = df['date'].dt.date
```
