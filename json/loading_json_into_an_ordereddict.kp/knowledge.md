---
title: How can I load JSON into an ordereddict?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, you can use the json.load() function with the object\_pairs\_hook argument set to OrderedDict.
---

**Contents**

[TOC]

**Section 1: What is an OrderedDict?**

An OrderedDict is a type of dictionary in which the elements are stored in the same order in which they were inserted. This means that when iterating through the elements, they will be returned in the same order they were inserted. 

**Section 2: How to Load JSON into an OrderedDict**

One way to load JSON into an OrderedDict is to use the json.loads() function. This function takes a JSON string and returns a Python dictionary object. The dictionary object can then be converted to an OrderedDict using the collections.OrderedDict() constructor. 

**Section 3: Example Code**

The following example code demonstrates how to load JSON into an OrderedDict:

```
import json
from collections import OrderedDict

# Load the JSON string
json_string = '{"name": "John", "age": 30}'

# Convert the JSON string to a dictionary
data = json.loads(json_string)

# Convert the dictionary to an OrderedDict
ordered_dict = OrderedDict(data)

# Print the OrderedDict
print(ordered_dict)
```

**Section 4: Output**

The output of the example code will be an OrderedDict with the following contents:

OrderedDict([('name', 'John'), ('age', 30)])
