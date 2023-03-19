---
title: How can a list or series be added as a row to a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `loc` method to append a list or series as a row to a pandas DataFrame in Python.
---

**Contents**

[TOC]

## Introduction
A pandas DataFrame is a two-dimensional, size-mutable, and heterogeneous data structure with columns that can be of different data types such as numeric, object, datetime, and categorical. It is very useful for data manipulation and analysis in Python. In this tutorial, we will discuss how to append a list or a series to a pandas DataFrame as a row in Python.

## Appending a list to a pandas DataFrame
To append a list to a pandas DataFrame as a new row, we can use the `loc` attribute and assign the list to it. Here is an example:

```python
import pandas as pd

# create a dataframe
df = pd.DataFrame(columns=['A', 'B'])

# create a list to append
row = [1, 2]

# append the list to the dataframe
df.loc[len(df)] = row

print(df)
```

Output:
```
   A  B
0  1  2
```

In the above code, we first create an empty DataFrame with columns ‘A’ and ‘B’. We then create a list called `row` that we want to append to the DataFrame. Finally, we use the `loc` attribute and assign the list to it.

## Appending a series to a pandas DataFrame
To append a series to a pandas DataFrame as a new row, we can use the `append` method of the DataFrame. Here is an example:

```python
import pandas as pd

# create a dataframe
df = pd.DataFrame(columns=['A', 'B'])

# create a series to append
row = pd.Series(data=[1, 2], index=df.columns)

# append the series to the dataframe
df = df.append(row, ignore_index=True)

print(df)
```

Output:
```
   A  B
0  1  2
```

In the above code, we first create an empty DataFrame with columns ‘A’ and ‘B’. We then create a series called `row` that we want to append to the DataFrame. We specify the index of the series to be the same as the DataFrame columns using `df.columns`. Finally, we use the `append` method and pass the `row` series to it along with the `ignore_index=True` parameter to reset the index of the DataFrame.

## Appending multiple rows to a pandas DataFrame
To append multiple rows to a pandas DataFrame, we can use either the `loc` attribute or the `append` method in a loop. Here is an example using the `append` method:

```python
import pandas as pd

# create a dataframe
df = pd.DataFrame(columns=['A', 'B'])

# create a list of lists to append
rows = [[1, 2], 
        [3, 4], 
        [5, 6]]

# append the rows to the dataframe
for row in rows:
    s = pd.Series(row, index=df.columns)
    df = df.append(s, ignore_index=True)

print(df)
```

Output:
```
   A  B
0  1  2
1  3  4
2  5  6
```

In the above code, we first create an empty DataFrame with columns ‘A’ and ‘B’. We then create a list of lists called `rows` with the rows that we want to append to the DataFrame. We then loop through each list in `rows`, convert it to a series with the index being the same as dataframe columns using `pd.Series(row, index=df.columns)`, and append it to the DataFrame using the `append` method. Finally, we reset the index of the DataFrame using the `ignore_index=True` parameter of the `append` method.

## Conclusion
In this tutorial, we learned how to append a list or a series to a pandas DataFrame as a row in Python. We also learned how to append multiple rows to a DataFrame using a loop. By using these techniques, we can easily manipulate and analyze data in Python with the help of pandas DataFrames.
