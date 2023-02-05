---
title: Obtaining the month and year values independently from a pandas datetime column
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the pandas.Series.dt.strftime() method to extract the month and year from a Pandas Datetime column.
---

**Contents**

[TOC]

#### Section 1: Import Libraries

```python
import pandas as pd
```

#### Section 2: Create Dataframe

```python
#Create Dataframe
df = pd.DataFrame({'Date':['2019-11-05', '2019-12-25', '2020-01-01']})
```

#### Section 3: Extract Month and Year

```python
#Extract Month and Year
df['Month'] = df['Date'].dt.month
df['Year'] = df['Date'].dt.year
```

#### Section 4: Output

```python
#Output
print(df)
```

```
         Date  Month  Year
0  2019-11-05     11  2019
1  2019-12-25     12  2019
2  2020-01-01      1  2020
```
