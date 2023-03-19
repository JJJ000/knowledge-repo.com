---
title: How to create Python xml elementtree object from a string source?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The xml ElementTree can be created from a string source using the `fromstring()` method.
---

**Contents**

[TOC]

Section 1: Introduction to Python xml ElementTree
Python xml ElementTree is a Python library for processing XML (Extensible Markup Language) data structures. It is a simple and lightweight library that provides a tree-based representation of an XML document, and enables the efficient parsing and manipulation of XML data. The xml ElementTree library provides numerous XML-related functions, such as parsing XML files, extracting information from XML documents, and writing XML files.

Section 2: Parsing an XML string with Python xml ElementTree
One of the key functionalities of the xml ElementTree library is parsing XML strings. To parse an XML string, you can use the fromstring() method of the ElementTree class. This method takes a string containing a well-formed XML document, and returns an Element object representing the root element of the XML document. Here’s an example of how to parse an XML string with Python xml ElementTree:

import xml.etree.ElementTree as ET

xml_string = "<root><child>text</child></root>"
root = ET.fromstring(xml_string)

In this example, we first create an XML string containing a root element and a child element. We then use the fromstring() method to parse the XML string and create an Element object representing the root element. We can now access the various parts of the XML document using the Element object, for instance:

# Accessing the child element:
child = root.find('child')

# Accessing text inside the child element:
text = child.text

Section 3: Manipulating XML data with Python xml ElementTree
Once you have parsed an XML string into an Element object, you can start manipulating the XML data using various ElementTree functions. For example, you can add new elements to the XML document, modify existing elements, and delete elements. Here are a few examples of XML manipulation with Python xml ElementTree:

# Adding a new element to the XML document:
new_element = ET.Element('new_child')
new_element.text = 'new text'
root.append(new_element)

# Modifying an existing element's text:
child.text = 'new child text'

# Deleting an element from the XML document:
root.remove(child)

Section 4: Writing XML data to a file with Python xml ElementTree
Finally, once you have manipulated an XML document using Python xml ElementTree, you can write the modified XML data to a file. To do this, you can use the ElementTree’s write() method, which takes a filename as its argument. Here’s an example:

import xml.etree.ElementTree as ET

# Parse an XML string into an Element object
xml_string = "<root><child>text</child></root>"
root = ET.fromstring(xml_string)

# Modify the XML data
child = root.find('child')
child.text = 'new child text'

# Write the modified XML data to a file
tree = ET.ElementTree(root)
tree.write('output.xml')

In this example, we first create an Element object by parsing an XML string. We then modify the XML data by changing the text of an element. Finally, we create an ElementTree object, which represents the entire XML document, and use its write() method to write the modified XML data to a file. The resulting file will contain the modified XML data, with the original structure of the XML document preserved.
