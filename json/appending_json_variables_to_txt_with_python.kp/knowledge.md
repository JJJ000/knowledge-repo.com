---
title: Write the contents of a Python dictionary to a .txt file, with each item on a separate line
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the json.dump() method to write the JSON object to a .txt file, and add the separators parameter to add a new line for each variable.
---

**Contents**

[TOC]

# Section 1: Dumping JSON to a Text File

Python provides a built-in module, `json`, to encode and decode JSON data. To dump a JSON object to a text file, you can use the `json.dump()` method. This method takes two parameters: the JSON object and the file object to which the JSON should be written.

For example, consider the following JSON object:

```
data = {
    "name": "John Smith",
    "age": 25,
    "city": "New York"
}
```

To dump this object to a text file, you can use the following code:

```
import json

with open('data.txt', 'w') as f:
    json.dump(data, f)
```

# Section 2: Appending Variables to a Text File

If you want to append each variable from the JSON object to a text file on a new line, you can use the `json.dumps()` method. This method takes the JSON object as a parameter and returns a string representation of the object.

For example, to append each variable from the above JSON object to a text file, you can use the following code:

```
import json

with open('data.txt', 'a') as f:
    for key, value in data.items():
        f.write(json.dumps(key) + '\n')
        f.write(json.dumps(value) + '\n')
```

# Section 3: Writing Variables to a Text File in JSON Format

If you want to write each variable from the JSON object to a text file in JSON format, you can use the `json.dump()` method. This method takes the JSON object as a parameter and returns a string representation of the object.

For example, to write each variable from the above JSON object to a text file in JSON format, you can use the following code:

```
import json

with open('data.txt', 'a') as f:
    for key, value in data.items():
        f.write(json.dumps({key: value}) + '\n')
```

# Section 4: Writing Variables to a Text File in Pretty-Printed JSON Format

If you want to write each variable from the JSON object to a text file in a pretty-printed JSON format, you can use the `json.dump()` method with the `indent` parameter. This method takes the JSON object as a parameter and returns a string representation of the object in a pretty-printed format.

For example, to write each variable from the above JSON object to a text file in a pretty-printed JSON format, you can use the following code:

```
import json

with open('data.txt', 'a') as f:
    for key, value in data.items():
        json.dump({key: value}, f, indent=4)
        f.write('\n')
```
