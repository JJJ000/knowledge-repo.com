---
title: What is the process for saving json data to a file in Python?
authors:
- cool_wizard
tags:
- python
- json
- knowledge
thumbnail: images/python.png
created_at: 2023-01-15 00:00:00
updated_at: 2023-01-15 00:00:00
tldr: Use the `json.dump()` function to write JSON data to a file.
---

**Contents**

[TOC]

### Import the Necessary Modules

In order to write JSON data to a file, you will need to import the `json` module.

```python
import json
```

### Create Your Data

Next, create the data that you wish to write to the file. This data should be in the form of a Python dictionary or list.

```python
data = {
    "name": "John Doe",
    "age": 25,
    "city": "New York"
}
```

### Write the Data to the File

Now that you have your data, you can write it to the file. To do this, open the file in write mode and use the `json.dump` method to write the data.

```python
with open('data.json', 'w') as f:
    json.dump(data, f)
```

### Verify the Data Was Written

Finally, you can verify that the data was written correctly by opening the file and printing the contents.

```python
with open('data.json', 'r') as f:
    data = json.load(f)
    print(data)
```
