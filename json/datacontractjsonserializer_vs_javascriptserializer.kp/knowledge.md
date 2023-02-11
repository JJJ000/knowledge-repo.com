---
title: What are the distinctions between datacontractjsonserializer and javascriptserializer?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: DataContractJsonSerializer is a serializer from the .NET framework that is used to serialize and deserialize objects into JSON, while JavaScriptSerializer is a serializer used in JavaScript to serialize and deserialize objects into JSON.
---

**Contents**

[TOC]

**Serialization Format**

DataContractJsonSerializer: XML

JavaScriptSerializer: JSON

**Features**

DataContractJsonSerializer: Supports serializing and deserializing of objects, including those with inheritance and type information.

JavaScriptSerializer: Supports serializing and deserializing of objects, including those with complex types.

**Performance**

DataContractJsonSerializer: Has a slower performance than JavaScriptSerializer.

JavaScriptSerializer: Has a faster performance than DataContractJsonSerializer.

**Usage**

DataContractJsonSerializer: Is typically used in applications that require a high degree of control over the serialization process, such as when interoperability with other systems is needed.

JavaScriptSerializer: Is typically used in applications that require a simpler, more lightweight serialization process, such as when working with AJAX or web services.
