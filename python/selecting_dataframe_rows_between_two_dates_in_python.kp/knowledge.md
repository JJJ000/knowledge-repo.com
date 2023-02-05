---
title: Retrieve rows from a dataframe between two specified dates
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the DataFrame.loc[] method to select rows between two dates.
---

**Contents**

[TOC]

#### Section 1: Import Libraries

```python
import pandas as pd
import numpy as np
```

#### Section 2: Create a DataFrame

```python
# Create a DataFrame
df = pd.DataFrame({'date': ['2020-01-01', '2020-01-02', '2020-01-03', '2020-01-04', '2020-01-05', '2020-01-06'],
                   'value': [1, 2, 3, 4, 5, 6]})
```

#### Section 3: Select Rows Between Two Dates

```python
# Select rows between two dates
start_date = '2020-01-02'
end_date = '2020-01-05'
mask = (df['date'] > start_date) & (df['date'] <= end_date)
df_between_dates = df.loc[mask]
```

#### Section 4: Print the DataFrame

```python
# Print the DataFrame
print(df_between_dates)
```

Output:

|    | date       | value |
|---:|:-----------|------:|
|  1 | 2020-01-02 |     2 |
|  2 | 2020-01-03 |     3 |
|  3 | 2020-01-04 |     4 |
|  4 | 2020-01-05 |     5 |
