---
title: Print JSON data in a pretty format to a file using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Python can be used to pretty-print JSON data to a file using the json.dump() function.
---

**Contents**

[TOC]

# Section 1: Importing Libraries

In order to pretty-print JSON data to a file using Python, we will need to import the json library. This library will allow us to read and write JSON data.

```python
import json
```

# Section 2: Opening the File

Next, we will need to open the file that we want to write the JSON data to. We will use the `open()` function to do this.

```python
with open('file_name.json', 'w') as f:
```

# Section 3: Writing the Data

Now that we have opened the file, we can write the JSON data to it. We will use the `json.dump()` function to do this.

```python
json.dump(data, f, indent=4)
```

# Section 4: Closing the File

Finally, we will need to close the file. We can do this using the `close()` function.

```python
f.close()
```
