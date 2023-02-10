---
title: What is the process for transforming an xml string into a dictionary?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Use a library such as xmltodict to convert an XML string to a dictionary in JSON.
---

**Contents**

[TOC]

1. Prerequisites
----------------
Before you start, you will need to install the Python library `xmltodict` with the command:

`pip install xmltodict`

2. Parsing the XML
------------------
Once you have the library installed, you can parse the XML string with the following code:

```python
import xmltodict

xml_string = '<root><element>value</element></root>'

dict_from_xml = xmltodict.parse(xml_string)
```

3. Converting to JSON
---------------------
Once you have the dictionary object, you can convert it to a JSON string with the following code:

```python
import json

json_string = json.dumps(dict_from_xml)
```

4. Output
---------
The final output will be a JSON string containing the data from the XML string:

`{"root": {"element": "value"}}`
