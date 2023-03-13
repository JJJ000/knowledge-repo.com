---
title: What is the process for appending a suffix (or prefix) to every column name?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Add the suffix to all column names using the .add\_suffix() method or add the prefix to all column names using the .add\_prefix() method.
---

**Contents**

[TOC]

Section 1: Importing necessary libraries
In order to add suffix (or prefix) to column names in Python, we need to use the pandas library. Therefore, let's start by importing the necessary libraries:

```python
import pandas as pd
```

Section 2: Reading in data
Now, let's assume that we have a dataset that we want to add a suffix (or prefix) to its column names. We will read in this dataset using the `read_csv()` function from pandas. Here's an example:

```python
data = pd.read_csv('example_data.csv')
```

For the purpose of this example, let's say that this dataset looks like this:
```
   id  age  gender
0   1   24    male
1   2   32  female
2   3   45    male
3   4   21  female
```

Section 3: Adding suffix (or prefix) to column names
Now that we have our data loaded, we can add suffix (or prefix) to the column names using the `add_suffix()` or `add_prefix()` function from pandas. Here's an example on how to add a suffix "_new" to each column name:

```python
data = data.add_suffix('_new')
```

This will change the column names in our example data to:

```
   id_new  age_new  gender_new
0       1       24        male
1       2       32      female
2       3       45        male
3       4       21      female
```

Similarly, we can use `add_prefix()` function to add a prefix to each column name. Here's an example on how to add a prefix "new_" to each column name:

```python
data = data.add_prefix('new_')
```

This will change the column names in our example data to:

```
   new_id  new_age  new_gender
0       1       24        male
1       2       32      female
2       3       45        male
3       4       21      female
```

Section 4: Saving data
Finally, if we want to save the modified data to a new csv file, we can use the `to_csv()` function from pandas. Here's an example:

```python
data.to_csv('modified_data.csv', index=False)
```

This will save the modified data to the file named "modified_data.csv" in the current directory, with the row index excluded from the output file.
