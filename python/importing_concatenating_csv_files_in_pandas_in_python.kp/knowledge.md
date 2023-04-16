---
title: Combine multiple csv files into a single dataframe using pandas' import and concatenation functions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the pandas.concat() function to concatenate multiple CSV files into one DataFrame.
---

**Contents**

[TOC]

**Section 1: Import CSV Files**

The first step is to import the CSV files into pandas. This can be done by using the pandas library and the read_csv() function. 

```
import pandas as pd

df1 = pd.read_csv("file1.csv")
df2 = pd.read_csv("file2.csv")
```

**Section 2: Concatenate DataFrames**

Once the CSV files have been imported, they can be concatenated into a single DataFrame. This can be done by using the pandas concat() function.

```
df = pd.concat([df1, df2])
```

**Section 3: Examine DataFrame**

It is important to examine the DataFrame to ensure that it has been concatenated properly. This can be done by using the head() and tail() functions.

```
df.head()
df.tail()
```

**Section 4: Save DataFrame**

Finally, the concatenated DataFrame can be saved as a CSV file. This can be done by using the to_csv() function.

```
df.to_csv("concatenated_data.csv")
```
