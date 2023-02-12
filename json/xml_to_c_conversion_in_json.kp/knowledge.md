---
title: Transforming an xml document into a c# object that can be manipulated dynamically
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: XML can be deserialized into a dynamic C# object using the Newtonsoft.Json library.
---

**Contents**

[TOC]

# Section 1: Deserializing XML
Deserializing XML is the process of converting XML documents into a dynamic C# object. This can be done by using the XmlSerializer class in the System.Xml.Serialization namespace. The XmlSerializer class provides methods for serializing objects into XML documents and deserializing XML documents into objects. 

# Section 2: Converting XML to Json
Once the XML document has been deserialized, it can be converted to Json using the Newtonsoft Json.NET library. The JsonConvert.SerializeXmlNode method can be used to convert the XML document into a Json string. 

# Section 3: Working with the Json String
Once the XML document has been converted to Json, it can be manipulated and accessed as a dynamic C# object. This can be done by using the JObject class in the Newtonsoft Json.NET library. The JObject class provides methods for parsing and manipulating Json strings.

# Section 4: Using the Dynamic C# Object
Once the Json string has been parsed into a dynamic C# object, it can be used to access and manipulate the data. This can be done by using the dynamic keyword in C#. The dynamic keyword allows for the use of dynamic method invocation and dynamic member access.
