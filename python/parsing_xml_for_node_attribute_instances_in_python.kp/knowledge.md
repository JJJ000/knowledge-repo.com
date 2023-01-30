---
title: What is the process for extracting a specific attribute from an xml node?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the xml.etree.ElementTree module to parse XML and get instances of a particular node attribute in Python.
---

**Contents**

[TOC]

## Section 1: Import Libraries

The first step is to import the necessary libraries. In this case, we will need the `xml.etree.ElementTree` library to parse the XML data.

```python
import xml.etree.ElementTree as ET
```

## Section 2: Parse XML

Once the necessary library has been imported, we can use the `parse` method to parse the XML data.

```python
tree = ET.parse("input.xml")
```

## Section 3: Get Instances of Node Attribute

Once the XML data has been parsed, we can use the `findall` method to find all instances of a particular node attribute.

```python
nodes = tree.findall(".//node[@attribute]")
```

## Section 4: Iterate Through Nodes

Finally, we can iterate through the nodes to get the values of the node attributes.

```python
for node in nodes:
    attribute_value = node.attrib["attribute"]
    print(attribute_value)
```
