---
title: Convert a list of objects to JSON using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Python can convert a list of objects to JSON using the json.dumps() method.
---

**Contents**

[TOC]

#### Section 1: Creating the List of Objects 

A list of objects can be created in Python by providing a list of comma-separated values within square brackets. For example, let's say you want to create a list of objects that represent a student's grades:

```
grades = [
    {'subject': 'Math', 'grade': 90},
    {'subject': 'English', 'grade': 85},
    {'subject': 'Science', 'grade': 95}
]
```

#### Section 2: Converting List of Objects to JSON

The list of objects can be converted to JSON using the `json.dumps()` method. This method takes the list of objects as an argument and returns a JSON string representation of the data.

```
import json

json_data = json.dumps(grades)
```

#### Section 3: Inspecting the JSON Output

The JSON output of the `json.dumps()` method can be inspected to verify that the data was properly converted to JSON.

```
print(json_data)

[{"subject": "Math", "grade": 90}, {"subject": "English", "grade": 85}, {"subject": "Science", "grade": 95}]
```

#### Section 4: Saving the JSON Output

The JSON output can be saved to a file for later use. This can be done using the `json.dump()` method, which takes a file object as an argument and writes the JSON data to the file.

```
with open('grades.json', 'w') as fp:
    json.dump(json_data, fp)
```
