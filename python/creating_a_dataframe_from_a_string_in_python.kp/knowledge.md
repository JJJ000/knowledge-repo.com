---
title: Construct a pandas dataframe from a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Pandas DataFrame can be created from a string by using the pandas.read\_csv() function.
---

**Contents**

[TOC]

### Section 1: Importing Libraries

```python
import pandas as pd
```

### Section 2: Defining the String

```python
data_string = 'Name: John; Age: 25; City: New York'
```

### Section 3: Creating the DataFrame

```python
data_list = data_string.split(';')

data_dict = {}

for item in data_list:
    key, value = item.split(':')
    data_dict[key.strip()] = value.strip()

df = pd.DataFrame(data_dict, index=[0])
```

### Section 4: Output

```python
print(df)
```

Output:

| Name | Age | City |
|------|-----|------|
| John | 25  | New York |
