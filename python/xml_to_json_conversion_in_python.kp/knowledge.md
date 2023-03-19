---
title: How to use Python to transform xml into json?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: One way to convert XML to JSON using Python is to use the xmltodict module.
---

**Contents**

[TOC]

## Importing Required Libraries

```python
import json
import xmltodict
```

We first start by importing the `json` and `xmltodict` libraries.

## Converting XML to a Python Dictionary

```python
with open('input.xml') as xml_file:
    data_dict = xmltodict.parse(xml_file.read())
    xml_file.close()
```

We start by reading the input XML file and parsing it using the `xmltodict` library. This turns the XML file into a Python dictionary that we can work with.

## Converting Python Dictionary to JSON

```python
json_data = json.dumps(data_dict, indent=4)
```

Finally, we use the `json` library to convert the Python dictionary into a JSON string. The `indent` argument is optional and just adds indentation to the output JSON file to make it easier to read.

## Writing JSON to an Output File

```python
with open('output.json', 'w') as json_file:
    json_file.write(json_data)
    json_file.close()
```

We can then save the JSON string to an output file using the `write` method from Python's file object. This will save the JSON in the format of a string in a .json file.
