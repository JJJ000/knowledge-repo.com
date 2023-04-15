---
title: Rephrased how to group a pandas dataframe by the month of a datetime column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To group a Pandas DataFrame by month in Python, use the pd.Grouper with the frequency set to `M`.
---

**Contents**

[TOC]

### Section 1: Creating a Sample DataFrame

Pandas is a powerful Python library used for data manipulation and analysis. Before we can perform the `groupby` operation, let's first create a sample DataFrame.

``` python
import pandas as pd
import numpy as np

rng = pd.date_range(start='1/1/2020', end='12/31/2020', freq='D')
df = pd.DataFrame({'date': rng, 'value': np.random.randint(0,100,size=(len(rng)))})

print(df.head())
```
Output:

```
        date  value
0 2020-01-01     50
1 2020-01-02     33
2 2020-01-03     85
3 2020-01-04     62
4 2020-01-05     66
```

We have created a DataFrame with two columns, `date` and `value`. The date column has a range of dates from 1st January 2020 to 31st December 2020, and the value column has randomly generated integer values ranging from 0 to 100.

### Section 2: Grouping DataFrame by Month

Now that we have a sample DataFrame, let's group it by month using the `groupby` function in Pandas.

``` python
df_monthly = df.groupby(pd.Grouper(key='date', freq='M')).sum().reset_index()
print(df_monthly.head())
```

Output:

```
        date  value
0 2020-01-31   1595
1 2020-02-29   1358
2 2020-03-31   1461
3 2020-04-30   1429
4 2020-05-31   1555
```

In the above code, we have used `pd.Grouper` function to group the DataFrame by month. The key parameter is set to `'date'` column which is the column we want to group by. The `freq` parameter is set to `'M'`, which indicates that we want to group the DataFrame by month. The `sum()` function is used to sum the values in each month, and `reset_index()` function is used to convert the grouped data back to a DataFrame.

### Section 3: Visualizing the Grouped Data

We can visualize the grouped data using various plotting libraries. 

``` python
import matplotlib.pyplot as plt

plt.plot(df_monthly['date'], df_monthly['value'])
plt.xlabel('Month')
plt.ylabel('Sum of Values')
plt.show()
```

Output:

![plot](https://i.imgur.com/bxrKA5Z.png)

In the above code, we have used `matplotlib` library to plot the data. We have plotted the sum of the values in each month on the y-axis, and the month on the x-axis. 

### Section 4: Conclusion

In this tutorial, we have learned how to group a Pandas DataFrame by month using the `groupby` function. Grouping data by time intervals is a common operation in data analysis, and Pandas provides an easy way to perform this operation using the `pd.Grouper` function. Once the data is grouped, it can be easily visualized using Python's powerful plotting libraries.
