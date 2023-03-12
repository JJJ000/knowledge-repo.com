---
title: What is the process of transforming sql query output into pandas data structure?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the pandas.read\_sql\_query() function to convert SQL query result to pandas data structure.
---

**Contents**

[TOC]

## Section 1: Connect to Database

To query a SQL database from Python, you first need to establish a connection. In this section, we will install the necessary libraries, and then connect to our database.

```python
!pip install pandas
!pip install sqlalchemy
!pip install psycopg2

import pandas as pd
from sqlalchemy import create_engine

# Initialize the database connection
engine = create_engine('postgresql://user:password@host:port/database')
```
## Section 2: Query the Database

To query the database, we will use the `read_sql_query()` method, which takes two arguments: the SQL query and the database connection. We will store the query result in a Pandas DataFrame.

```python
# Example SQL query
query = 'SELECT * FROM my_table'

# Query the database and store the result in a DataFrame
df = pd.read_sql_query(query, engine)

# Preview the data
df.head()
```

## Section 3: Clean and Transform the Data

After retrieving the data from the database, we may need to clean and transform it before using it for analysis. We can use Pandas methods such as `dropna()`, `fillna()`, `apply()`, and `groupby()` to clean and transform the data as needed.

``` python
# Example: remove records with missing values
df_clean = df.dropna()

# Example: transform text data to lower case
df_clean['column_name'] = df_clean['column_name'].apply(lambda x: x.lower())

# Example: calculate the mean value of a column by group
df_grouped = df_clean.groupby('group_column')['numeric_column'].mean()
```

## Section 4: Export the Data as CSV or Excel File

Finally, we can export the cleaned and transformed data as a CSV or Excel file using the `to_csv()` or `to_excel()` method.

``` python
# Example: export the data as a CSV file
df_clean.to_csv('cleaned_data.csv', index=False)

# Example: export the data as an Excel file
df_grouped.to_excel('grouped_data.xlsx', index=False)
```
