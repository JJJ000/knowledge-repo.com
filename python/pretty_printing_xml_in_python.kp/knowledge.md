---
title: Printing xml in a formatted manner using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The xml.dom.minidom library can be used to pretty print XML in Python.
---

**Contents**

[TOC]

### Using the xml.dom.minidom Library
The xml.dom.minidom library is a Python library that allows for easy manipulation of XML documents. It can be used to pretty print XML by using the toprettyxml() method.

### Example Code
Below is an example of how the xml.dom.minidom library can be used to pretty print an XML document:

```python
from xml.dom import minidom

# Open the XML document
doc = minidom.parse("sample.xml")

# Pretty print the XML document
print(doc.toprettyxml())
```

### Output
The output of the above code will be a nicely formatted and indented XML document.

### Other Libraries
In addition to the xml.dom.minidom library, there are other libraries that can be used to pretty print XML documents, such as lxml and BeautifulSoup.
