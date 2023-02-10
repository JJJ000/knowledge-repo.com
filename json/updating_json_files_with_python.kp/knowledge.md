---
title: How can I use Python to modify a JSON file?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON module to read, modify, and write the JSON file.
---

**Contents**

[TOC]

# Section 1: Read the JSON File

The first step in updating a JSON file with Python is to read the JSON file. This can be done using the json module. The json.load() function will read the JSON file and return a Python dictionary. 

```python
import json

with open('data.json') as json_file:
    data = json.load(json_file)
```

# Section 2: Update the Data

Once the data has been read into a Python dictionary, it can be updated by modifying the values of the dictionary. For example, if we wanted to add a new key-value pair to the data, we could do so by simply adding it to the dictionary. 

```python
data['new_key'] = 'new_value'
```

# Section 3: Write the Updated Data

Once the data has been updated, it needs to be written back to the JSON file. This can be done using the json.dump() function. 

```python
with open('data.json', 'w') as json_file:
    json.dump(data, json_file)
```

# Section 4: Close the JSON File

Finally, the JSON file needs to be closed. This can be done using the close() method. 

```python
json_file.close()
```
