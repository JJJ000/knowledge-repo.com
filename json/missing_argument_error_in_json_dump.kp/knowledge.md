---
title: The json.dump() function in Python requires one positional argument, 'fp', to be specified
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The dump() function requires a file object to be passed as an argument to write the JSON data.
---

**Contents**

[TOC]

## What is the Error?
The error message is `TypeError: json.dump() missing 1 required positional argument: 'fp'`. This error occurs when the `json.dump()` function is used without specifying an output file.

## What is json.dump()?
The `json.dump()` function is part of the Python json module. It is used to write a Python object into a JSON file. This function takes two parameters: `obj` and `fp`. The `obj` parameter is the Python object to be written to the file, and the `fp` parameter is the file object to which the data is written.

## How to Fix the Error
To fix this error, the `fp` parameter must be specified when using the `json.dump()` function. This can be done by opening a file object in write mode and passing it as the `fp` parameter. For example:

```
import json

data = {
    'name': 'John Doe',
    'age': 30,
    'occupation': 'Software Engineer'
}

with open('data.json', 'w') as fp:
    json.dump(data, fp)
```

In the example above, the `fp` parameter is specified as the file object `fp`, which was opened in write mode. This will write the Python object `data` to the file `data.json`.
