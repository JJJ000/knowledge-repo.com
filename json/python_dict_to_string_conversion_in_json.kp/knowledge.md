---
title: Change a Python dictionary into a string and then back into a dictionary
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can convert a Python dict to a JSON string using the json.dumps() method, and convert a JSON string back to a Python dict using the json.loads() method.
---

**Contents**

[TOC]

#### Converting a Python Dict to a String in JSON

The `json.dumps()` method can be used to convert a Python dictionary to a string in JSON format. This method takes in the dictionary as an argument and returns a JSON string. 

```python
import json

my_dict = {'name': 'John', 'age': 25}
json_str = json.dumps(my_dict)
print(json_str)
```

The output of the above code will be:

`{"name": "John", "age": 25}`

#### Converting a String in JSON to a Python Dict

The `json.loads()` method can be used to convert a string in JSON format to a Python dictionary. This method takes in the JSON string as an argument and returns a Python dictionary. 

```python
import json

json_str = '{"name": "John", "age": 25}'
my_dict = json.loads(json_str)
print(my_dict)
```

The output of the above code will be:

`{'name': 'John', 'age': 25}`
