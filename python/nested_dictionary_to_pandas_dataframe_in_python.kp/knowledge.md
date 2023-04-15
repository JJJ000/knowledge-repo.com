---
title: Create a pandas dataframe using the elements contained in a nested dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use pd.DataFrame.from\_dict() to construct a pandas DataFrame from the items in a nested dictionary in Python.
---

**Contents**

[TOC]

## **Section 1: Understanding the problem statement**

Before we dive into the solution, let's first understand the problem statement. We have a nested dictionary that contains data in a hierarchical format. Our task is to extract that data and store it in a pandas DataFrame object, which is a more structured and organized way of representing data.

## **Section 2: Data Preparation**

To prepare the data for the DataFrame conversion, we first need to flatten the nested dictionary. We can use a recursive function to traverse the dictionary and append the data to a list. 

```
data = {'a': {'x': 1, 'y': 2}, 'b': {'x': 3, 'y': 4}}
keys = ['k1', 'k2']
rows = []

def flatten_dict(d, key_list):
    for k, v in d.items():
        new_key_list = key_list + [k]
        if isinstance(v, dict):
            flatten_dict(v, new_key_list)
        else:
            rows.append(new_key_list + [v])

for k, v in data.items():
    flatten_dict(v, [k])
```
In this code snippet, we initialize an empty list `rows` to store the flattened data. We then define the `flatten_dict` function that takes in a dictionary `d` and a list of keys `key_list`. If the value of a key-value pair in the dictionary is a nested dictionary, we recursively call the function with the updated `key_list`. Otherwise, we append a flattened row to the `rows` list.

## **Section 3: Creating the DataFrame**

Now that we have the flattened data, we can create the pandas DataFrame object. We'll first create a list of column names by combining the original dictionary keys and the nested keys. We'll then create the DataFrame using the flattened `rows` list and the column names.

```
import pandas as pd

columns = list(data.keys()) + list(data[list(data.keys())[0]].keys())
df = pd.DataFrame(rows, columns=columns)
```

In this code snippet, we create the `columns` list by combining the top-level keys in the original dictionary with the nested dictionary keys. We then create a DataFrame object `df` using the flattened `rows` list and the `columns` list as column names.

## **Section 4: Putting it all together**

Here's the final solution that combines all the code snippets we've discussed so far:

```
data = {'a': {'x': 1, 'y': 2}, 'b': {'x': 3, 'y': 4}}
keys = ['k1', 'k2']
rows = []

def flatten_dict(d, key_list):
    for k, v in d.items():
        new_key_list = key_list + [k]
        if isinstance(v, dict):
            flatten_dict(v, new_key_list)
        else:
            rows.append(new_key_list + [v])

for k, v in data.items():
    flatten_dict(v, [k])

columns = list(data.keys()) + list(data[list(data.keys())[0]].keys())
df = pd.DataFrame(rows, columns=columns)
```

This solution should work for any nested dictionary with a similar structure as the one we've described here.
