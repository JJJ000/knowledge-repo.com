---
title: Verify the presence of a key and loop through the JSON array using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Yes, you can use a for loop to iterate through the JSON array and check if the key exists.
---

**Contents**

[TOC]

**Section 1: Checking if a Key Exists in a JSON Object**

We can use the `in` keyword to check if a key exists in a JSON object. For example:

```python
import json

data = {
    "name": "John Doe",
    "age": 30
}

if "name" in data:
    print("Name key exists!")
```

**Section 2: Iterating Through a JSON Array**

We can use a `for` loop to iterate through a JSON array. For example:

```python
import json

data = [
    {
        "name": "John Doe",
        "age": 30
    },
    {
        "name": "Jane Doe",
        "age": 25
    }
]

for person in data:
    print("Name: " + person["name"])
    print("Age: " + str(person["age"]))
```

**Section 3: Accessing a Specific Item in a JSON Array**

We can use the `index` operator to access a specific item in a JSON array. For example:

```python
import json

data = [
    {
        "name": "John Doe",
        "age": 30
    },
    {
        "name": "Jane Doe",
        "age": 25
    }
]

person = data[1]

print("Name: " + person["name"])
print("Age: " + str(person["age"]))
```

**Section 4: Finding the Index of a Specific Item in a JSON Array**

We can use the `enumerate` function to find the index of a specific item in a JSON array. For example:

```python
import json

data = [
    {
        "name": "John Doe",
        "age": 30
    },
    {
        "name": "Jane Doe",
        "age": 25
    }
]

for index, person in enumerate(data):
    if person["name"] == "Jane Doe":
        print("Jane Doe is at index " + str(index))
```
