---
title: Substituting the header with the first row
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: There is no difference between a header and a top row in Python, they both refer to the first row of a data table.
---

**Contents**

[TOC]

Section 1: Introduction

In many data analysis or manipulation tasks, we often come across headers and top rows that serve some purpose. Headers are usually the names of columns or variables while the top rows may contain some critical information such as the units of measurements, data source, or data range. However, sometimes we may want to replace headers with top rows for data cleaning or structuring. In this article, we will discuss various methods to replace headers with top rows in Python.

Section 2: Reading Data with Top Rows as Headers

One way to replace headers with top rows is to read the data file in a way that treats the top row as headers. This approach can be useful if the first row contains all the column names and no additional information. We can achieve this using the `header` parameter while reading data with pandas `read_csv()` method. Here is an example code:

```python
import pandas as pd
df = pd.read_csv('data.csv', header=0)  
```

In this code, we are reading a CSV file named 'data.csv' and specifying that the first row should be treated as headers using the `header=0` parameter. This will replace the default column names (0,1,2,...) with the names present in the top row. 

Section 3: Replacing Headers with Top Rows

Another way to replace headers with top rows is to extract the top row, save it as a list, and set it as headers of the dataframe. In this method, we can keep the original index or reset it as needed. Here is an example code:

```python
import pandas as pd
df = pd.read_csv('data.csv') # read the data
headers = list(df.iloc[0, :]) # extract the top row as a list
df = df.iloc[1:, :] # remove the top row
df.columns = headers # set the top row as headers
```

In this code, we are reading a CSV file 'data.csv', extracting the top row as a list, removing the top row from the dataframe, and then setting the top row as headers using the `columns` attribute of the dataframe. This method works well if we want to manipulate the top row separately or if we need to reset the index.

Section 4: Conclusion

Replacing headers with top rows is a simple yet crucial step in data cleaning and manipulation. We have discussed two methods to achieve this in Python - reading data with top rows as headers using the `header` parameter and replacing headers with top rows by setting a list as column names. Choose the method that suits your needs and keep exploring the vast possibilities of Python in data science and analysis.
