---
title: Loading multiple JSON documents into a pandas dataframe
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Pandas can read multiple JSON records into a dataframe using the `read\_json` function.
---

**Contents**

[TOC]

#### Section 1: Read the JSON File

We can read a JSON file into a Pandas dataframe using the `read_json()` method. The `read_json()` method takes a file path or a URL as an argument and returns a Pandas dataframe.

```python
import pandas as pd

df = pd.read_json('file_name.json')
```

#### Section 2: Check the Dataframe

Once the dataframe is created, it's important to check that it contains the expected data. We can use the `info()` and `head()` methods to get a quick overview of the data.

```python
df.info()
df.head()
```

#### Section 3: Manipulate the Dataframe

Once we have confirmed that the dataframe contains the expected data, we can manipulate it further. We can add or remove columns, sort the data, or perform other operations.

```python
# Add a new column
df['new_column'] = 'value'

# Sort the data
df.sort_values(by='column_name', ascending=True, inplace=True)
```

#### Section 4: Export the Dataframe

Once the dataframe is ready, we can export it to a file. We can use the `to_json()` method to export the dataframe to a JSON file.

```python
df.to_json('file_name.json', orient='records')
```
