---
title: Retrieving values from JSON using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON module`s `loads()` and `get()` functions to extract values from a JSON object.
---

**Contents**

[TOC]

**Section 1: Importing the JSON Library**

In order to get values from JSON using Python, we first need to import the JSON library. This can be done with the following code:

```python
import json
```

**Section 2: Loading the JSON File**

Once the JSON library is imported, we can then load the JSON file using the `load()` method. This method takes a file object as its argument and returns a Python dictionary object.

```python
with open('data.json') as f:
    data = json.load(f)
```

**Section 3: Accessing Values in the JSON File**

Once the JSON file is loaded, we can then access the values in the file using the `[]` operator. For example, if we wanted to access the value of the "name" key in the JSON file, we would use the following code:

```python
name = data['name']
```

**Section 4: Working with Nested Data**

If the JSON file contains nested data, we can access the values in the same way. For example, if we wanted to access the value of the "age" key in a nested dictionary, we would use the following code:

```python
age = data['person']['age']
```
