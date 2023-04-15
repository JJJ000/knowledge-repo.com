---
title: How to prevent columns from being duplicated while using pandas merge?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Specify the columns to merge on and drop the duplicated columns using the `drop` method or by specifying which columns to keep using the `merge` function with the `suffixes` parameter.
---

**Contents**

[TOC]

Section 1: Introduction
When working with large data sets, it is often necessary to combine data from different sources. The Pandas library in Python provides several methods to combine data, including the merge function. However, when merging data, it is possible to end up with duplicate columns, which can make the data confusing and difficult to work with. In this article, we will discuss how to avoid duplicating columns when merging data in Pandas.

Section 2: Using the suffix parameter
One way to avoid duplicating columns in Pandas is to use the suffix parameter when merging two data frames. The suffix parameter allows you to specify a string to be added to the end of the column names in case of a name conflict. Here is an example:

```
import pandas as pd

# create two data frames with a common column
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df2 = pd.DataFrame({'A': [4, 5, 6], 'C': [7, 8, 9]})

# merge the data frames using the common column
merged_df = pd.merge(df1, df2, on='A', suffixes=('_1', '_2'))
print(merged_df)
```

In this example, we have two data frames with a common column 'A'. We merge the data frames using the merge function, and specify the 'A' column as the join key. We also specify suffixes='_1' and '_2' to be added to the column names of the two data frames in case of a name conflict. The resulting merged data frame will have columns 'A_1', 'B', 'A_2', and 'C', where 'A_1' and 'A_2' are the 'A' columns from the original data frames, and 'B' and 'C' are the remaining columns.

Section 3: Using the join method
Another way to avoid duplicating columns in Pandas is to use the join method instead of the merge function. The join method is a convenience method that is equivalent to calling merge with the join key specified as the index of the two data frames. Here is an example:

```
import pandas as pd

# create two data frames with a common column
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]}).set_index('A')
df2 = pd.DataFrame({'C': [7, 8, 9]}, index=[4, 5, 6])

# join the data frames using the index
joined_df = df1.join(df2)
print(joined_df)
```

In this example, we create two data frames with a common column 'A'. We use the set_index method to set the 'A' column as the index of the first data frame, and create the second data frame with an index that matches the values in the 'A' column. We then call the join method on the first data frame, passing the second data frame as an argument. Since we have specified the index as the join key, the resulting joined data frame will have one column 'B' and one column 'C', with the 'A' column dropped.

Section 4: Renaming columns after the merge
Finally, if you end up with duplicate columns after merging data in Pandas, you can always rename the columns to make them unique. Here is an example:

```
import pandas as pd

# create two data frames with a common column
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df2 = pd.DataFrame({'A': [4, 5, 6], 'B': [7, 8, 9]})

# merge the data frames using the common column
merged_df = pd.merge(df1, df2, on='A')

# rename the columns to make them unique
merged_df = merged_df.rename(columns={'B_x': 'B_1', 'B_y': 'B_2'})

print(merged_df)
```

In this example, we have two data frames with a common column 'A' and a duplicate column 'B'. We merge the data frames using the merge function and the 'A' column as the join key. We end up with duplicate columns 'B_x' and 'B_y'. To make the column names unique, we call the rename method on the merged data frame, passing a dictionary that maps the old column names to new column names. The resulting merged data frame will have columns 'A', 'B_1', and 'B_2'.
