---
title: Converting a list into a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: A list can be serialized to JSON by using the json.dumps() method.
---

**Contents**

[TOC]

### Section 1: Importing Libraries

The first step to serializing a list to JSON in Python is to import the `json` library.

```python
import json
```

### Section 2: Creating a List

The next step is to create a list that will be serialized.

```python
my_list = ["item1", "item2", "item3"]
```

### Section 3: Serializing the List

Once the list is created, it can be serialized to JSON.

```python
serialized_list = json.dumps(my_list)
```

### Section 4: Outputting the Serialized List

The final step is to output the serialized list.

```python
print(serialized_list)
```
