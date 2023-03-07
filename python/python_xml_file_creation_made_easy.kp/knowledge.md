---
title: Generating an elementary xml document utilizing python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To create a simple XML file using python, use the ElementTree module and its methods like Element, SubElement, and ElementTree to define the structure and content of the file.
---

**Contents**

[TOC]

# Introduction
XML stands for Extensible Markup Language, which is a markup language that is both human-readable and machine-readable. In this tutorial, we will discuss how to create a simple XML file using Python.

# Step 1: Importing the required modules
We need to import the ElementTree module to create XML documents. ElementTree is a Python library that is used to manipulate XML files. 

```python
import xml.etree.ElementTree as ET
```

# Step 2: Creating an XML document
To create an XML document, we first need to create a root element. We can do this using the Element() function from the ElementTree module. We can also add child elements to the root element using the SubElement() function.

```python
root = ET.Element("students")

student1 = ET.SubElement(root, "student")
student1.set("name", "John")
student1.set("age", "25")

student2 = ET.SubElement(root, "student")
student2.set("name", "Jane")
student2.set("age", "23")

tree = ET.ElementTree(root)
tree.write("students.xml")
```

In this example, we created an XML document with the root element "students". We then added two child elements "student" to the root element, with their respective attributes as "name" and "age". Finally, we wrote the XML document to a file named "students.xml".

# Step 3: Viewing the XML document
After running the Python script, we should be able to view the outputted XML file. Here is the contents of "students.xml":

```xml
<students>
    <student age="25" name="John" />
    <student age="23" name="Jane" />
</students>
```

# Conclusion
Creating an XML file using Python is easy with the help of the ElementTree module. We can create an XML document by creating a root element and adding child elements to it. This can be used to generate a variety of XML documents, including configuration files, data interchange formats, and more.
