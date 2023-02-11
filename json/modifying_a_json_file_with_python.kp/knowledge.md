---
title: Edit a JSON file using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Yes, it is possible to read a JSON file using Python and modify it using the JSON library.
---

**Contents**

[TOC]

# Section 1: Reading a JSON File

Reading a JSON file is relatively easy in Python. To do this, we use the `json` library and the `open` function.

```
import json

with open('file.json') as json_file:
    data = json.load(json_file)
```

This reads the contents of the JSON file into a Python dictionary, which can then be accessed and manipulated.

# Section 2: Modifying a JSON File

Once the JSON file has been read into a Python dictionary, it can be modified by accessing the relevant keys and changing their values. For example, if we wanted to change the value of a key called `name`, we could do the following:

```
data['name'] = 'New Name'
```

# Section 3: Writing the Modified JSON File

Once the JSON file has been modified, it must be written back to the file. This is done using the `json` library's `dump` function.

```
with open('file.json', 'w') as json_file:
    json.dump(data, json_file)
```

# Section 4: Conclusion

In conclusion, reading and modifying a JSON file in Python is relatively straightforward. Using the `json` library and the `open` and `dump` functions, we can easily read and modify JSON files.
