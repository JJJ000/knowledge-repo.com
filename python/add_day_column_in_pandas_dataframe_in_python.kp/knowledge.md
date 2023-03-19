---
title: Create a new column in a pandas dataframe that calculates the number of days between two dates
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can create a new column in a DataFrame pandas in Python by subtracting two columns of dates and converting the resulting Timedelta objects to integers using the dt.days attribute.
---

**Contents**

[TOC]

## Importing the Pandas Module

First we need to import the pandas module in Python. We can do this using the import statement as follows:

```python
import pandas as pd
```

## Reading the CSV file

Next, we need to read a CSV file using pandas `read_csv()` function. The CSV file can be read as follows:

```python
df = pd.read_csv('file.csv')
```

## Adding the Column

Lastly, we can add the column containing the number of days between two dates using the `DateOffset` and `apply` functions in pandas:

```python
from pandas.tseries.offsets import DateOffset

df['Days'] = (df['End_Date'] - df['Start_Date']).apply(lambda x: x / pd.Timedelta(days=1))
```

Here, we imported the `DateOffset` function from `pandas.tseries.offsets` module, then we created a new column `Days` and calculated the number of days between `End_Date` and `Start_Date` columns using the `apply` function.

The `apply` function applies a function to each element of a pandas series, and in this case, we used a lambda function to divide the timedelta object by one day, which returns the number of days.

Thus, the `Days` column is added to the DataFrame with the number of days between dates.
