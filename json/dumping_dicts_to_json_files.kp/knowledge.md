---
title: What is the process for saving a dictionary to a JSON file?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.dump() method to dump a dict to a JSON file.
---

**Contents**

[TOC]

### Section 1: Create a Dict

To dump a dict to a JSON file, you must first create a dict. A dict is a collection of key-value pairs. For example:

```
my_dict = {
  "name": "John Doe",
  "age": 30,
  "city": "New York"
}
```

### Section 2: Import the JSON Module

Once you have your dict, you need to import the JSON module. This module provides functions for encoding and decoding JSON data.

```
import json
```

### Section 3: Dump the Dict to a JSON File

Now you can use the json.dump() function to dump the dict to a JSON file. This function takes two arguments: the dict to be dumped and the file object to which the JSON data will be written.

```
with open('my_dict.json', 'w') as f:
  json.dump(my_dict, f)
```

### Section 4: Verify the JSON File

Finally, you can verify that the JSON file was created correctly by opening it in a text editor. The contents should look something like this:

```
{
  "name": "John Doe",
  "age": 30,
  "city": "New York"
}
```
