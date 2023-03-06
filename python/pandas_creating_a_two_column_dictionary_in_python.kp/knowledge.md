---
title: What is the process to generate a dictionary containing two columns from pandas dataframes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the to\_dict() method with the parameters `key` and `value` as the column names.
---

**Contents**

[TOC]

## Section 1: Introduction
When you have two columns in a pandas DataFrame that you want to combine into a dictionary, you can use the `to_dict()` method provided by pandas. The `to_dict()` method will convert the DataFrame into a Python dictionary, and you can specify the column(s) to use as keys and the column(s) to use as values. 

## Section 2: Example Data
For this example, we'll create a simple pandas DataFrame with two columns, "fruit" and "color":

```python
import pandas as pd

data = {
    "fruit": ["apple", "banana", "orange", "kiwi"],
    "color": ["red", "yellow", "orange", "green"]
}

df = pd.DataFrame(data)
```

## Section 3: Creating the Dictionary
To create a dictionary using the "fruit" column as keys and the "color" column as values, we can use the following code:

```python
fruit_color_dict = df.set_index('fruit').to_dict()['color']
```

Let's break this down:

1. `set_index('fruit')` sets the "fruit" column as the DataFrame index, which means it will become the keys in the resulting dictionary.
2. `to_dict()` converts the DataFrame to a dictionary.
3. `['color']` selects the "color" column as the values in the resulting dictionary.

Now we have a dictionary that looks like this:

```python
{
    'apple': 'red',
    'banana': 'yellow',
    'orange': 'orange',
    'kiwi': 'green'
}
```

## Section 4: Conclusion
Creating a dictionary from two pandas DataFrame columns is a simple process using the `to_dict()` method. By specifying the column(s) to use as keys and the column(s) to use as values, you can quickly transform your DataFrame into a dictionary that can be used for further analysis or visualization.
