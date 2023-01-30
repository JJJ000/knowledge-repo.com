---
title: Saving a pandas dataframe as a csv file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the DataFrame.to\_csv() method to write a pandas DataFrame to a CSV file.
---

**Contents**

[TOC]

##### Step 1: Import Libraries

```python
import pandas as pd
```

##### Step 2: Create a DataFrame

```python
data = {'Name':['Tom', 'nick', 'krish', 'jack'], 'Age':[20, 21, 19, 18]} 
df = pd.DataFrame(data)
```

##### Step 3: Write DataFrame to CSV

```python
df.to_csv('sample.csv', index=False)
```

##### Step 4: Check CSV File

The CSV file can be checked using a text editor or spreadsheet application.
