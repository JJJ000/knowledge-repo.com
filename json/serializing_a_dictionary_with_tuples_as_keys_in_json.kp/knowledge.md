---
title: Serialize a dictionary containing tuples as keys into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: A dictionary with tuples as keys can be serialized to JSON using the json.dumps() method.
---

**Contents**

[TOC]

1. Create the Dictionary 

A dictionary with tuples as keys can be created in Python as follows:

```
my_dict = {(1,2): 'value1', (3,4): 'value2', (5,6): 'value3'}
```

2. Serialize the Dictionary

The dictionary can be serialized to JSON using the json module in Python:

```
import json

serialized_dict = json.dumps(my_dict)
```

3. Output the Serialized Dictionary

The serialized dictionary can be printed to the console or written to a file:

```
print(serialized_dict)  # Prints '{"(1, 2)": "value1", "(3, 4)": "value2", "(5, 6)": "value3"}'

with open('my_dict.json', 'w') as f:
    json.dump(serialized_dict, f)  # Writes the serialized dictionary to the file 'my_dict.json'
```

4. Deserialize the Dictionary

The serialized dictionary can be deserialized back to its original form using the json module in Python:

```
deserialized_dict = json.loads(serialized_dict)
```
