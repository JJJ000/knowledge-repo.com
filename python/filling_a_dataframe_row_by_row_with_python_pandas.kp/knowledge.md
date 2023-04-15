---
title: How to add data to a pandas dataframe one row at a time using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To fill a dataframe row by row in pandas, you can either iterate through the rows using a for loop or use the DataFrame.loc() method to specify the row index and column names to fill in the values.
---

**Contents**

[TOC]

Section 1: Creating an empty dataframe
To fill a dataframe row by row, we need to first create an empty dataframe with the required columns. We can use the pandas DataFrame() constructor to create an empty dataframe as follows:

```python
import pandas as pd

# Create an empty dataframe with columns
df = pd.DataFrame(columns=['column1', 'column2', 'column3'])
```

Section 2: Appending rows to the dataframe
Once we have created an empty dataframe with the required columns, we can append rows to the dataframe using the append() method of the pandas dataframe. We can append rows as dictionaries, where the keys correspond to the column names and values correspond to the data we want to fill in each row.

```python
# Append rows to the empty dataframe
df = df.append({'column1': 'value1', 'column2': 'value2', 'column3': 'value3'}, ignore_index=True)
df = df.append({'column1': 'value4', 'column2': 'value5', 'column3': 'value6'}, ignore_index=True)
```

In the above example, we have appended two rows to the dataframe, where 'value1', 'value2', and 'value3' are the data we want to fill in the first row, and 'value4', 'value5', and 'value6' are the data we want to fill in the second row. The ignore_index=True parameter ensures that each appended row gets a unique index value.

Section 3: Using loops to fill the dataframe row by row
In some cases, we may want to fill the dataframe row by row using loops instead of appending rows one by one. In such cases, we can use a for loop to iterate through the rows and fill in the data for each row.

```python
# Using a for loop to fill the dataframe row by row
for i in range(n_rows):
    row_data = get_row_data(i)  # Function to get data for a single row
    df = df.append(row_data, ignore_index=True)
```

In the above example, we are using a for loop to iterate through 'n_rows' and use the 'get_row_data()' function to get the data for each row. We are then appending each row of data to the dataframe using the append() method.

Section 4: Conclusion
In this tutorial, we have learned how to fill a pandas dataframe row by row by first creating an empty dataframe with the required columns and then appending rows to the dataframe using the append() method or using loops to fill the dataframe row by row.
