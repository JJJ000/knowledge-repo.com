---
title: Python implementation for converting JSON to xml
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the xml.etree.ElementTree module in Python to parse the JSON data into an XML file.
---

**Contents**

[TOC]

## Introduction
JSON is a lightweight data interchange format while XML is a markup language which is designed to store and transport data. The conversion of JSON to XML format is a useful procedure in data processing. In this tutorial, we will walk you through the process of converting JSON to XML using Python.

## Converting JSON to XML using Python’s xml.etree.ElementTree module
Python’s xml.etree.ElementTree module provides easy-to-use methods to create, modify, and transfer XML data. We can use this module to convert JSON to XML. To convert JSON to XML, we need to follow the steps below:

1. Create a dictionary to hold the JSON data.
2. Create an Element object and set its tag name to the root element of the XML data.
3. Iterate through the key-value pairs of the dictionary, create SubElement objects, and set their tag name to the keys.
4. Append the corresponding values to the SubElement objects.
5. Use the tostring() method to create an XML string from the Element object.

Here is an example:

```python
import json
import xml.etree.ElementTree as ET

# JSON string
json_str = '{"name": "Emily", "age": 25, "city": "New York"}'

# Convert JSON to dictionary
json_dict = json.loads(json_str)

# Create Element object for XML
root = ET.Element('Person')

# Iterate through dictionary and create SubElement objects
for key, value in json_dict.items():
    child = ET.SubElement(root, key)
    child.text = str(value)

# Convert Element object to XML string
xml_str = ET.tostring(root)

print(xml_str)
```

Output:

```xml
b'<Person><name>Emily</name><age>25</age><city>New York</city></Person>'
```

## Converting JSON to XML using xmltodict module
The xmltodict module is a third-party module that simplifies the conversion of JSON to XML. It converts JSON data to a Python dictionary and then converts the dictionary to an XML string using Python’s xml.etree.ElementTree module. Here is an example:

```python
import json
import xmltodict

# JSON string
json_str = '{"name": "Emily", "age": 25, "city": "New York"}'

# Convert JSON to dictionary
json_dict = json.loads(json_str)

# Convert dictionary to XML string
xml_str = xmltodict.unparse({'Person': json_dict})

print(xml_str)
```

Output:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Person>
  <name>Emily</name>
  <age>25</age>
  <city>New York</city>
</Person>
```

## Conclusion
In this tutorial, we have shown two ways to convert JSON to XML using Python. The xml.etree.ElementTree module provides a way to create, modify, and transfer XML data, while the xmltodict module simplifies the conversion using Python’s xml.etree.ElementTree module. These methods can be used for various data processing tasks in Python.
