---
title: Include the absent dates in the pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: One way to add missing dates to a pandas dataframe in Python is to use the `reindex` function with a date range as the new index.
---

**Contents**

[TOC]

1. Introduction

When working with a pandas dataframe, it is common to find missing dates in the index or columns. These missing dates can create gaps in the data that can affect the analysis and visualization. In this tutorial, we will show how to add missing dates to a pandas dataframe in Python.

2. Creating a sample dataframe

Let's create a sample dataframe to work with. This dataframe will have missing dates in the index.

```
import pandas as pd
import numpy as np

dates = pd.date_range('20210101', '20210110')
data = np.random.randn(len(dates))
df = pd.DataFrame({'data': data}, index=dates)

# add some missing dates
df = df.drop(df.index[[2, 5, 8]])
```

The resulting dataframe will have missing dates in the index.

```
               data
2021-01-01 -0.611398
2021-01-02 -0.231912
2021-01-04 -0.284156
2021-01-06  0.368989
2021-01-07 -0.747178
2021-01-09 -2.381941
2021-01-10 -1.514232
```

3. Resampling the dataframe

To add missing dates to the dataframe, we need to resample it using the `resample()` method. This method groups the data by a specific frequency and applies a function to each group. In this case, we will use the `asfreq()` function to convert the data to a specified frequency and fill the missing dates with `NaN` values.

```
freq = 'D'
df = df.resample(freq).asfreq()
```

The `freq` variable specifies the frequency of the resampled data. In this case, we are using a daily frequency. The `asfreq()` function converts the data to the specified frequency and fills the missing dates with `NaN` values.

4. Filling missing values

To fill the missing values, we can use the `fillna()` method. We can specify a value to fill the missing values or use the method `ffill()` to forward fill the missing values with the last known value.

```
df = df.fillna(method='ffill')
```

The resulting dataframe will have the missing dates filled with the last known value.

```
               data
2021-01-01 -0.611398
2021-01-02 -0.231912
2021-01-03 -0.231912
2021-01-04 -0.284156
2021-01-05 -0.284156
2021-01-06  0.368989
2021-01-07 -0.747178
2021-01-08 -0.747178
2021-01-09 -2.381941
2021-01-10 -1.514232
```

5. Conclusion

In this tutorial, we have shown how to add missing dates to a pandas dataframe in Python. We have used the `resample()` method to convert the data to a specified frequency and fill the missing dates with `NaN` values. We have also used the `fillna()` method to fill the missing values with a specified value or the last known value.
