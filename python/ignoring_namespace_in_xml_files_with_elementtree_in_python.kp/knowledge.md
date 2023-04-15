---
title: How to use the 'find' and 'findall' method in python's elementtree module to locate matching elements in xml files, while ignoring their namespace
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a wildcard character (`*`) as the namespace in the element name, for example, element = root.find(`.//{namespaceuri}*/{element\_name}`).
---

**Contents**

[TOC]

## Introduction
ElementTree is a Python library used for parsing XML data. It provides a simple way to parse and navigate through the XML document. However, sometimes XML documents contain namespaces which can make it difficult to find matching elements using the `find` and `findall` methods. This article describes how to ignore the namespace of XML files to locate matching elements when using the `find` and `findall` methods in the ElementTree module.

## Using XPath expressions without namespace
One solution to ignore the namespace is to use XPath expressions without namespace prefix. In XPath, you can use the `local-name()` function to match elements by their local names only. Here's an example:

```python
import xml.etree.ElementTree as ET

tree = ET.parse('file.xml')
root = tree.getroot()

# find all elements with tag name 'element_name'
elements = root.findall(".//*[local-name()='element_name']")
for element in elements:
    print(element.text)
```

In this example, we first parse the XML file using `ET.parse()` and get the root element using `tree.getroot()`. Then we use `root.findall()` to find all elements with the tag name 'element_name' using an XPath expression with the `local-name()` function.

## Removing namespaces from XML
Another solution is to remove the namespaces from the XML document using a regular expression. Here's an example:

```python
import re
import xml.etree.ElementTree as ET

# read the XML file as a string
with open('file.xml', 'r') as file:
    xml_string = file.read()

# remove the namespaces using regular expressions
xml_string = re.sub(r'\sxmlns="[^"]+"', '', xml_string, count=1)

# parse the modified XML string
root = ET.fromstring(xml_string)

# find all elements with tag name 'element_name'
elements = root.findall(".//element_name")
for element in elements:
    print(element.text)
```

In this example, we first read the XML file as a string and remove the namespaces using regular expressions. Then we parse the modified XML string using `ET.fromstring()` and get the root element. Finally, we use `root.findall()` to find all elements with the tag name 'element_name' directly, without using an XPath expression.

## Using a namespace map
A third solution is to use a namespace map to map the XML namespace to a prefix. Here's an example:

```python
import xml.etree.ElementTree as ET

tree = ET.parse('file.xml')
root = tree.getroot()

# define the namespace map
nsmap = {'ns': 'http://example.com/namespace'}

# find all elements with tag name 'element_name'
elements = root.findall('.//ns:element_name', namespaces=nsmap)
for element in elements:
    print(element.text)
```

In this example, we first parse the XML file using `ET.parse()` and get the root element using `tree.getroot()`. Then we define a namespace map with a prefix 'ns' that maps to the XML namespace 'http://example.com/namespace'. Finally, we use `root.findall()` to find all elements with the tag name 'element_name' using an XPath expression with the 'ns' prefix and the `namespaces` argument to pass the namespace map.

## Conclusion
In this article, we have discussed three ways to ignore the namespace of XML files to locate matching elements when using the `find` and `findall` methods in the ElementTree module. These include using XPath expressions without namespace prefix, removing namespaces from XML using a regular expression, and using a namespace map. Developers may choose any of these solutions based on their specific requirement.
