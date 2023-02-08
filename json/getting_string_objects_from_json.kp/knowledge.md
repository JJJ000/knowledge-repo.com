---
title: How can I get string objects instead of unicode when parsing json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.dumps() method with the ensure\_ascii parameter set to False.
---

**Contents**

[TOC]

**Section 1: Import json module**

The first step is to import the json module into your code. This can be done using the following code:

```python
import json
```

**Section 2: Load the JSON data**

Once the json module is imported, you can load the JSON data using the json.load() method. For example, if you have a file called mydata.json, you can load the data using the following code:

```python
with open('mydata.json') as f:
    data = json.load(f)
```

**Section 3: Parse the JSON data**

Once the JSON data is loaded, you can parse the data to get the desired output. To get string objects instead of Unicode, you can use the json.loads() method. For example, if you have a JSON string stored in a variable called my_json_string, you can parse it using the following code:

```python
data = json.loads(my_json_string)
```

**Section 4: Access the string objects**

Once the JSON data is parsed, you can access the string objects using the appropriate keys. For example, if you have a JSON object with a key called “name”, you can access the value using the following code:

```python
name = data['name']
```
