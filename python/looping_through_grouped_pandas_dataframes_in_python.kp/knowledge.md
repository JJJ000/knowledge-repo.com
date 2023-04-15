---
title: What is the method to iterate through a pandas dataframe that has been grouped?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the groupby() function to group the dataframe by a specified column, then iterate over the groups using a for-loop.
---

**Contents**

[TOC]

### Section 1: Importing necessary libraries and creating sample dataframe
We first import the required libraries for this task - pandas and numpy. We then create a sample dataframe on which we will perform the loop operation. 

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({
    'Group': ['Group A', 'Group A', 'Group B', 'Group B', 'Group B', 'Group C','Group C','Group C'],
    'Values': [1, 2, 3, 4, 5, 6, 7, 8]
})
```

### Section 2: Grouping the dataframe
Before looping over the dataframe, we need to group the dataframe based on the values in the 'Group' column. We can use the 'groupby' method from pandas for this purpose. 

```python
grouped_df = df.groupby(['Group'])
```

### Section 3: Looping over the grouped dataframe
After grouping the dataframe, we can loop over each group using a for loop. We can obtain the group name and the group contents using the 'groups' and 'get_group' methods respectively. 

```python
for group_name, df_group in grouped_df:
    print('\nGroup:', group_name)
    print(df_group)
```

### Section 4: Putting it all together
The complete code for looping over a grouped pandas dataframe is as follows:

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({
    'Group': ['Group A', 'Group A', 'Group B', 'Group B', 'Group B', 'Group C','Group C','Group C'],
    'Values': [1, 2, 3, 4, 5, 6, 7, 8]
})

grouped_df = df.groupby(['Group'])

for group_name, df_group in grouped_df:
    print('\nGroup:', group_name)
    print(df_group)
```
