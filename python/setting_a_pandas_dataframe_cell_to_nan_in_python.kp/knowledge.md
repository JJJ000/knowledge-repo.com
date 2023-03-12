---
title: What are the steps to assign nan value to a cell in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To set a cell to NaN in a pandas dataframe, use the syntax `df.loc[row\_index, column\_index] = np.nan`, where `df` is the dataframe, `row\_index` is the index of the row, `column\_index` is the index of the column, and `np.nan` is the NaN value from the NumPy library.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is a popular data manipulation library in Python, widely used for data analysis and data exploration tasks. The library offers a wide range of functionalities for data processing, including data cleaning, data transformation, and data manipulation. One of the essential features that Pandas offers is the ability to handle missing or null data, commonly represented by NaN (Not a Number) values. In this tutorial, we will explore how to set a cell to NaN in a Pandas dataframe in Python.

Section 2: Creating a Pandas DataFrame
The first step before setting a cell to NaN is to create a Pandas dataframe. We can create a Dataframe using the Pandas library, and there are multiple ways to create it. Here, we will create a simple dataframe with some data:

```python
import pandas as pd
import numpy as np

# defining dictionary
data = {'Name': ['John', 'David', 'David', 'Marry', 'Robert'],
        'Age': [27, 24, 26, 22, 32],
        'City': ['New York', 'Paris', 'London', 'Los Angeles', 'San Francisco'],
        'Country': ['USA', 'France', 'UK', 'USA', 'USA']}

# Creating dataframe from dictionary
df = pd.DataFrame(data)
```


Section 3: Setting a cell to NaN
After creating the dataframe, we can set a cell to NaN by using various methods. Here are some ways to do that:

Method 1: Setting a cell to NaN by index and column label
We can set a particular cell to NaN based on its index and column label by using the loc property of the Dataframe.

```python
df.loc[2, 'Age'] = np.nan
```


Method 2: Setting a cell to NaN by conditional selection
We can also set a specific cell to NaN based on a particular condition.

```python
df.loc[df['Name'] == 'David', 'City'] = np.nan
```

In this example, we set the value of the 'City' column to NaN for all the rows where the 'Name' column is 'David'. 

Method 3: Setting multiple cells to NaN
We can set multiple cells to NaN using slicing or Boolean indexing.

``` python
df.loc[1:3, 'Age':'City'] = np.nan
```

In this example, we set the values of the columns 'Age' and 'City' to NaN for the rows 1 to 3 (inclusive) using the loc property of the Dataframe. We can also use Boolean indexing to achieve the same result.

``` python
df[df['Age'] > 25] = np.nan
```


Section 4: Conclusion
In this tutorial, we learned how to set a cell to NaN in a Pandas dataframe in Python. We saw that we could use the loc property of the Dataframe, Boolean indexing, and slicing to set a cell or multiple cells to NaN. Handling missing or null data is an essential aspect of data manipulation and cleaning, and the Pandas library provides various functionalities to help us with that.
