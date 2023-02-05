---
title: What is the syntax for adding a column to a specific location in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To insert a column at a specific column index in pandas, use the DataFrame.insert() method.
---

**Contents**

[TOC]

#### Section 1: Import Pandas

Begin by importing the pandas library. This will allow you to use the features of pandas to insert a column at a specific column index.

```python
import pandas as pd
```

#### Section 2: Create DataFrame

Create a DataFrame with the desired columns. 

```python
data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],'Age':[28,34,29,42]}
df = pd.DataFrame(data)
print(df)
```

The above code will create a DataFrame with two columns: Name and Age. 

#### Section 3: Insert Column

Use the insert() method to insert a column at a specific column index. The syntax for the insert() method is: 

```python
DataFrame.insert(loc, column, value, allow_duplicates = False)
```

For example, to insert a column at index 2 (third column):

```python
df.insert(2, "Height", [6.2, 5.1, 6.0, 5.5], True)
```

The above code will insert a column named "Height" at index 2 with the given values.

#### Section 4: Print DataFrame

Finally, print the DataFrame to view the newly inserted column.

```python
print(df)
```

The output will be: 

|    | Name  | Age | Height |
|----|-------|-----|--------|
| 0  | Tom   | 28  | 6.2    |
| 1  | Jack  | 34  | 5.1    |
| 2  | Steve | 29  | 6.0    |
| 3  | Ricky | 42  | 5.5    |
