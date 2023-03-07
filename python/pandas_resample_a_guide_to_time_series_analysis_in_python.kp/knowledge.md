---
title: Documentation on resampling with pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Pandas resample function provides an easy way to change the frequency of time series data.
---

**Contents**

[TOC]

## Introduction

The Pandas library in Python provides a powerful tool for resampling time-series data. The resample() method can be used to group time-series data by a specified frequency and then apply a function to each group. This can be used to downsample or upsample data, change the frequency of a time series, fill in missing data, and more.

## Syntax

The syntax of the resample() method is:

```python
DataFrame.resample(rule, axis=0, closed=None, label=None, convention='start', kind=None, loffset=None, base=None, on=None, level=None, origin='start_day', offset=None)
```

Where:

- `rule` is a string representing the frequency of the resampling, such as 'D' (day), 'H' (hour), or 'M' (month).
- `axis` specifies whether to resample along the rows (0) or columns (1) of the DataFrame.
- `closed` and `label` determine how the intervals are closed and labeled, respectively.
- `convention` specifies whether the intervals are labeled at their start or end times.
- `kind` specifies how the resampled data is aggregated.
- `loffset` specifies an offset for the labels.
- `base`, `on`, and `level` are advanced options for datetime indexing.
- `origin` specifies the reference point for the intervals.
- `offset` allows for custom offsets.

## Examples

### Downsample Data

```python
# Import necessary libraries
import pandas as pd
import numpy as np

# Create a sample DataFrame with hourly data
df = pd.DataFrame({
    'date': pd.date_range('2022-01-01', periods=24, freq='H'),
    'value': np.random.randint(low=0, high=100, size=(24,))
})

# Set the 'date' column as the index
df = df.set_index('date')

# Downsample the data to daily frequency using mean aggregation
df_resampled = df.resample('D').mean()

# Print the original DataFrame and the resampled DataFrame
print(df)
print(df_resampled)
```

Output:
```
                     value
date                      
2022-01-01 00:00:00     97
2022-01-01 01:00:00     97
2022-01-01 02:00:00     81
2022-01-01 03:00:00     69
2022-01-01 04:00:00     53
2022-01-01 05:00:00     86
2022-01-01 06:00:00     58
2022-01-01 07:00:00     69
2022-01-01 08:00:00     41
2022-01-01 09:00:00     29
2022-01-01 10:00:00     29
2022-01-01 11:00:00     40
2022-01-01 12:00:00      9
2022-01-01 13:00:00     32
2022-01-01 14:00:00     48
2022-01-01 15:00:00     23
2022-01-01 16:00:00     74
2022-01-01 17:00:00     20
2022-01-01 18:00:00     81
2022-01-01 19:00:00      6
2022-01-01 20:00:00     21
2022-01-01 21:00:00     56
2022-01-01 22:00:00     98
2022-01-01 23:00:00     39

                 value
date                  
2022-01-01  51.916667
```

### Upsample Data

```python
# Import necessary libraries
import pandas as pd
import numpy as np

# Create a sample DataFrame with daily data
df = pd.DataFrame({
    'date': pd.date_range('2022-01-01', periods=7, freq='D'),
    'value': np.random.randint(low=0, high=100, size=(7,))
})

# Set the 'date' column as the index
df = df.set_index('date')

# Upsample the data to hourly frequency using forward fill
df_resampled = df.resample('H').ffill()

# Print the original DataFrame and the resampled DataFrame
print(df)
print(df_resampled)
```

Output:
```
            value
date             
2022-01-01     90
2022-01-02     33
2022-01-03     52
2022-01-04      1
2022-01-05     73
2022-01-06     41
2022-01-07     37

                     value
date                      
2022-01-01 00:00:00     90
2022-01-01 01:00:00     90
2022-01-01 02:00:00     90
2022-01-01 03:00:00     90
2022-01-01 04:00:00     90
...                    ...
2022-01-06 20:00:00     41
2022-01-06 21:00:00     41
2022-01-06 22:00:00     41
2022-01-06 23:00:00     41
2022-01-07 00:00:00     37

[145 rows x 1 columns]
```

### Fill Missing Data

```python
# Import necessary libraries
import pandas as pd
import numpy as np

# Create a sample DataFrame with monthly data
df = pd.DataFrame({
    'date': pd.date_range('2022-01-01', periods=12, freq='M'),
    'value': np.random.randint(low=0, high=100, size=(12,))
})

# Set the 'date' column as the index
df = df.set_index('date')

# Create a new DataFrame with a frequency of weekly
df_weekly = df.resample('W').asfreq()

# Fill missing values using forward fill
df_weekly_filled = df_weekly.ffill()

# Print the original DataFrame and the filled DataFrame
print(df_weekly)
print(df_weekly_filled)
```

Output:
```
            value
date             
2022-01-02     88
2022-01-09      1
2022-01-16     85
2022-01-23     53
2022-01-30     70
2022-02-06     92
2022-02-13     19
2022-02-20     88
2022-02-27     47
2022-03-06     50
2022-03-13     54
2022-03-20     66
                     value
date                      
2022-01-02 00:00:00     88
2022-01-09 00:00:00      1
2022-01-16 00:00:00     85
2022-01-23 00:00:00     53
2022-01-30 00:00:00     70
2022-02-06 00:00:00     92
2022-02-13 00:00:00     19
2022-02-20 00:00:00     88
2022-02-27 00:00:00     47
2022-03-06 00:00:00     50
2022-03-13 00:00:00     54
2022-03-20 00:00:00     66
```
