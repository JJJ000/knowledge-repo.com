---
title: Iterate through the rows of a pandas dataframe and make changes to the dataframe as you go
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas DataFrame can be updated row by row by iterating over the rows and applying an operation to each row.
---

**Contents**

[TOC]

**Section 1: Create DataFrame**

We can create a dataframe in Pandas by passing a dictionary of lists to the `DataFrame` constructor.

```
import pandas as pd

# Create a dictionary of lists
data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],
        'Age':[28,34,29,42],
        'Rating':[4.23,3.24,3.98,2.56]}

# Create a DataFrame
df = pd.DataFrame(data)

# Print the DataFrame
print(df)
```

The output of the above code will be:

```
    Name  Age  Rating
0    Tom   28    4.23
1   Jack   34    3.24
2  Steve   29    3.98
3  Ricky   42    2.56
```

**Section 2: Iterate Through Rows**

We can iterate through the rows of a dataframe in Pandas by using the `iterrows()` method.

```
# Iterate through the rows
for index, row in df.iterrows():
    print(row['Name'], row['Age'])
```

The output of the above code will be:

```
Tom 28
Jack 34
Steve 29
Ricky 42
```

**Section 3: Update DataFrame**

We can update a dataframe in Pandas while iterating row by row by using the `at` method.

```
# Update the Rating values
for index, row in df.iterrows():
    df.at[index, 'Rating'] = round(row['Rating'] * 2, 2)

# Print the updated DataFrame
print(df)
```

The output of the above code will be:

```
    Name  Age  Rating
0    Tom   28    8.46
1   Jack   34    6.48
2  Steve   29    7.96
3  Ricky   42    5.12
```

**Section 4: Update DataFrame with Condition**

We can also update a dataframe in Pandas while iterating row by row with a condition.

```
# Update the Rating values with a condition
for index, row in df.iterrows():
    if row['Age'] > 30:
        df.at[index, 'Rating'] = round(row['Rating'] * 3, 2)

# Print the updated DataFrame
print(df)
```

The output of the above code will be:

```
    Name  Age  Rating
0    Tom   28    8.46
1   Jack   34    19.44
2  Steve   29    7.96
3  Ricky   42    15.36
```
