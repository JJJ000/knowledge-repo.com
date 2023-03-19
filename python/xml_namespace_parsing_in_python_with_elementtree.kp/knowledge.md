---
title: Parsing xml containing namespace in Python using 'elementtree'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: When parsing XML with namespace in Python via `ElementTree`, use the namespace argument when calling the ElementTree.parse() function.
---

**Contents**

[TOC]

Section 1: Introduction to XML Namespace and ElementTree
---------------------------------------------------------
XML Namespace is a way of qualifying element and attribute names in XML documents using a URI (Uniform Resource Identifier). The URI is used to identify the namespace in which particular element and attribute names are defined. The namespace ensures that element and attribute names are unique and do not clash with those defined in other namespaces. 

ElementTree is a popular Python library for parsing and creating XML documents. It provides a lightweight and efficient API for navigating and manipulating XML trees.

Section 2: Parsing XML with Namespace using ElementTree
---------------------------------------------------------
When parsing an XML document that contains namespaces, ElementTree requires some additional steps to correctly access the elements and attributes. The first step is to register the namespace with ElementTree using the `register_namespace` method. This method takes two arguments, the first being a namespace prefix and the second being the URI of the namespace.

Once the namespace is registered, we can use the namespace prefix when accessing elements and attributes in the XML document.

```python
import xml.etree.ElementTree as ET

# Register the namespace
ET.register_namespace("ns", "http://example.com/ns")

# Parse the XML document
tree = ET.parse("example.xml")

# Access an element with a namespace prefix
root = tree.getroot()
elem = root.find("ns:element", {"ns": "http://example.com/ns"})

# Access an attribute with a namespace prefix
attr = elem.get("ns:attribute")
```

In the above example, we register the namespace prefix "ns" with the URI "http://example.com/ns". We then parse the XML document "example.xml" and access an element with the namespace prefix "ns" using the `find` method. We also access an attribute with the namespace prefix "ns" using the `get` method.

Section 3: Iterating over Elements with a Namespace
---------------------------------------------------
To iterate over elements in an XML document that contain a namespace, we use the namespace prefix in the `findall` method. For example, to iterate over all elements with the namespace prefix "ns":

```python
import xml.etree.ElementTree as ET

# Register the namespace
ET.register_namespace("ns", "http://example.com/ns")

# Parse the XML document
tree = ET.parse("example.xml")

# Iterate over elements with a namespace
root = tree.getroot()
for elem in root.findall("ns:*", {"ns": "http://example.com/ns"}):
    # Do something with the element
    pass
```

In the above example, we register the namespace prefix "ns" with the URI "http://example.com/ns". We then parse the XML document "example.xml" and iterate over all elements with the namespace prefix "ns" using the `findall` method. The `findall` method takes a namespace-prefix pattern as its first argument and a dictionary mapping namespace prefixes to URIs as its second argument.

Section 4: Conclusion
----------------------
In this tutorial, we learned how to parse an XML document with namespaces using ElementTree in Python. We covered how to register namespaces, access elements and attributes with namespaces, and iterate over elements with namespaces. With this knowledge, you can confidently parse and manipulate XML documents with namespaces using ElementTree in Python.
