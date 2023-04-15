---
title: What is the process for saving dataframe to a Postgres table?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the pandas to\_sql() method to write a DataFrame to a Postgres table in Python.
---

**Contents**

[TOC]

## Introduction

In this tutorial, we will walk through the steps to write a pandas DataFrame to a Postgres table using Python.

## Establishing Connection
Firstly, we need to establish a connection between Python and the PostgreSQL database using the `psycopg2` module.

```python
import psycopg2
conn = psycopg2.connect(database="database_name", user="username", password="password", host="hostname", port="port_number")
```

## Writing DataFrame to Postgres

Next, We can use the `to_sql` method in pandas to write the DataFrame to a Postgres table.

```python
import pandas as pd

sql = "INSERT INTO table_name (col1,col2,col3) VALUES(%s, %s, %s)"

df = pd.DataFrame({'col1': [1, 2], 'col2': [3, 4], 'col3': [5, 6]})
df = df[['col1', 'col2', 'col3']]
records = df.to_records(index=False)

cur = conn.cursor()
cur.executemany(sql, records)
conn.commit()
```

## Closing the Connection
Lastly, it is important to close the connection to the Postgres database when we are done. 

```python
conn.close()
```

This will ensure that the database resources are freed up and any changes that we made are persisted. 

## Conclusion
In this tutorial, we learned how to use Python, pandas, and the psycopg2 module to write a DataFrame to a Postgres table.
