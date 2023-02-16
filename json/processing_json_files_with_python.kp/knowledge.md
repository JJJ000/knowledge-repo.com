---
title: Read multiple JSON files from a directory using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: Use the glob module to get a list of all the JSON files in the folder, then read each file using the JSON module.
---

**Contents**

[TOC]

# Section 1: Import Libraries

In order to read multiple JSON files from a folder, we will need to import the `os`, `json`, and `glob` libraries.

```python
import os
import json
from glob import glob
```

# Section 2: Get the Path

We will need to get the path of the folder that contains the JSON files. We can use the `os` library to get the current working directory and then append the folder name to the path.

```python
# Get the current working directory
cwd = os.getcwd()

# Get the path of the folder that contains the JSON files
folder_path = os.path.join(cwd, 'folder_name')
```

# Section 3: Read the Files

We can use the `glob` library to get a list of all the JSON files in the folder and then loop through them to read the data.

```python
# Get a list of all the JSON files in the folder
json_files = glob(os.path.join(folder_path, '*.json'))

# Loop through the list of files and read the data
data = []
for json_file in json_files:
    with open(json_file) as f:
        data.append(json.load(f))
```

# Section 4: Access the Data

Once we have read the data from the JSON files, we can access it using the `data` variable.

```python
# Access the data
for item in data:
    print(item)
```
