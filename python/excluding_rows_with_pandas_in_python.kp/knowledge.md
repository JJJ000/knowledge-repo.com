---
title: Pandas get rows that are not present in the other dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `.isin()` method with the `~` operator to get rows which are NOT in the other dataframe.
---

**Contents**

[TOC]

#### Section 1: Create Dataframes

First, we need to create two dataframes with different data:

```python
import pandas as pd

df1 = pd.DataFrame({'A':[1,2,3,4], 'B':[5,6,7,8]})
df2 = pd.DataFrame({'A':[3,4,5,6], 'B':[7,8,9,10]})
```

#### Section 2: Merge Dataframes

Next, we need to merge the two dataframes:

```python
merged_df = pd.merge(df1, df2, on='A', how='outer')
```

#### Section 3: Find Rows NOT in Other Dataframe

Finally, we can use the `isin()` method to find the rows that are NOT in the other dataframe:

```python
not_in_df2 = merged_df[~merged_df['A'].isin(df2['A'])]
```

#### Section 4: Output Results

Now we can print the results:

```python
print(not_in_df2)
```

The output will be:
```
   A  B_x  B_y
0  1    5  NaN
2  2    7  NaN
```
