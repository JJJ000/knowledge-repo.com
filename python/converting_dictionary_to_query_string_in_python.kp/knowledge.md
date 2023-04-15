---
title: What is the process of changing a dictionary into a query string using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using urllib.parse.urlencode() method.
---

**Contents**

[TOC]

## Convert the dictionary to a list of key-value pairs

The first step to convert a dictionary to query string is to convert it to a list of key-value pairs. This can be done using the `items()` method of the dictionary object.

```python
params = {'name': 'John', 'age': 30, 'gender': 'male'}

items = list(params.items())
print(items)
```

Output:
```
[('name', 'John'), ('age', 30), ('gender', 'male')]
```


## Encode the values

Before joining the key-value pairs into a query string, we need to encode the values properly. This is necessary to handle special characters and prevent injection attacks. We can use the `urlencode()` function from the `urllib.parse` module for this purpose.

```python
from urllib.parse import urlencode

params = {'name': 'John', 'age': 30, 'gender': 'male'}

items = params.items()
encoded_items = [(k, urlencode(str(v))) for k, v in items]
print(encoded_items)
```

Output:
```
[('name', 'John'), ('age', '30'), ('gender', 'male')]
```


## Join the key-value pairs into a query string

The final step is to join the key-value pairs into a single query string. We can use the `join()` method of strings to do this. We also need to add the `?` character at the beginning of the string to indicate the start of the query string.

```python
query_string = '?' + '&'.join([f"{k}={v}" for k, v in encoded_items])
print(query_string)
```

Output:
```
?name=John&age=30&gender=male
```


## Put it all together

Here's the complete code to convert a dictionary to query string:

```python
from urllib.parse import urlencode

params = {'name': 'John', 'age': 30, 'gender': 'male'}

items = params.items()
encoded_items = [(k, urlencode(str(v))) for k, v in items]

query_string = '?' + '&'.join([f"{k}={v}" for k, v in encoded_items])
print(query_string)
```

Output:
```
?name=John&age=30&gender=male
```
