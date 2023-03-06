---
title: How to eliminate duplicate dictionaries from a Python list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use a list comprehension with a set inside to remove duplicate dictionaries in a list.
---

**Contents**

[TOC]

## Introduction
When working with lists in Python, it is common to come across a scenario where we have a list of dictionaries, and we want to remove the duplicates. This tutorial will cover different methods to remove duplicate dictionaries in a list using Python.

## Using a set and JSON
One way to remove duplicates is by converting the list of dictionaries to JSON strings and then using set() to remove the duplicates.

```python
import json

def remove_duplicates(data):
  seen = set()
  new_data = []
  for d in data:
      json_d = json.dumps(d, sort_keys=True)
      if json_d not in seen:
          new_data.append(d)
          seen.add(json_d)
  return new_data

# Usage
data = [
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 1, "name": "Alice"},
  {"id": 3, "name": "Charlie"}
]

unique_data = remove_duplicates(data)
print(unique_data)
```

Output:
```
[
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 3, "name": "Charlie"}
]
```

## Using a set and frozenset
Another way to remove duplicates is by converting each dictionary to a frozenset, which is immutable and can be placed into a set.

```python
def remove_duplicates_frozenset(data):
  seen = set()
  new_data = []
  for d in data:
      frozenset_d = frozenset(d.items())
      if frozenset_d not in seen:
          new_data.append(d)
          seen.add(frozenset_d)
  return new_data

# Usage
data = [
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 1, "name": "Alice"},
  {"id": 3, "name": "Charlie"}
]

unique_data = remove_duplicates_frozenset(data)
print(unique_data)
```

Output:
```
[
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 3, "name": "Charlie"}
]
```

## Using a list comprehension and a set of tuples
Another approach is by using a list comprehension and a set of tuples.

```python
def remove_duplicates_list_comprehension(data):
    unique = set()
    return [x for x in data if tuple(x.items()) not in unique and not unique.add(tuple(x.items()))]

# Usage
data = [
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 1, "name": "Alice"},
  {"id": 3, "name": "Charlie"}
]

unique_data = remove_duplicates_frozenset(data)
print(unique_data)
```

Output:
```
[
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 3, "name": "Charlie"}
]
```

## Using pandas
Finally, we can also use the pandas library to remove duplicates. This approach requires converting the list of dictionaries to a pandas DataFrame and then using the drop_duplicates method.

```python
import pandas as pd

def remove_duplicates_pandas(data):
  df = pd.DataFrame(data)
  return df.drop_duplicates().to_dict('records')

# Usage
data = [
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 1, "name": "Alice"},
  {"id": 3, "name": "Charlie"}
]

unique_data = remove_duplicates_pandas(data)
print(unique_data)
```

Output:
```
[
  {"id": 1, "name": "Alice"},
  {"id": 2, "name": "Bob"},
  {"id": 3, "name": "Charlie"}
]
```
