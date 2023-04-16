---
title: What is the process for appending pandas data to an existing csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the pandas.DataFrame.to\_csv() method to write the pandas DataFrame to a CSV file.
---

**Contents**

[TOC]

**Section 1: Import Libraries**

```python
import pandas as pd
import csv
```

**Section 2: Read Data**

```python
# Read the existing csv file
csv_file = pd.read_csv('sample.csv')

# Read the pandas data
pandas_data = pd.DataFrame({'Name':['John', 'Mia', 'Alex'], 
                            'Age':[25, 22, 24]})
```

**Section 3: Append Data**

```python
# Append the pandas data to the existing csv file
csv_file = csv_file.append(pandas_data, ignore_index=True)
```

**Section 4: Save Data**

```python
# Save the updated csv file
csv_file.to_csv('sample.csv', index=False)
```
