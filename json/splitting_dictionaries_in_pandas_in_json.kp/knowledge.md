---
title: Create separate columns from a pandas column containing dictionaries using the split/explode method
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Pandas can be used to convert a column of JSON dictionaries into separate columns by using the json\_normalize() function.
---

**Contents**

[TOC]

**Section 1: Loading the Data** 

We can begin by loading the data into a pandas DataFrame. We can use the `read_json()` method to read in the data.

```python
import pandas as pd

df = pd.read_json('data.json')
```

**Section 2: Explode the Dictionary Column**

Next, we can use the `explode()` method to split the column of dictionaries into separate columns. 

```python
df = df.explode('column_name')
```

**Section 3: Rename the Columns**

After exploding the column, we can rename the columns to make them easier to identify. 

```python
df = df.rename(columns={'column_name_1': 'column_name_A', 'column_name_2': 'column_name_B'})
```

**Section 4: Save the Data**

Finally, we can save the data to a new file. 

```python
df.to_json('data_exploded.json')
```
