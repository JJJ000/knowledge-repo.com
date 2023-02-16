---
title: It is not possible to convert the current JSON object (e.g. {"name""value"}) into a system.collections.generic.list"1 type
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: It is not possible to deserialize a JSON object into a List type.
---

**Contents**

[TOC]

##### Section 1: What is Deserialization?
Deserialization is the process of taking a stream of bytes or data and converting it into an object. It is the reverse process of serialization, which converts an object into a stream of bytes that can be stored or transmitted.

##### Section 2: Why Deserialization is Required?
Deserialization is required to convert the data stored in the form of strings or bytes into an object. This is useful when the data is to be used by an application or when the data needs to be stored in a file or database.

##### Section 3: How to Deserialize a JSON Object?
Deserializing a JSON object is possible using the Newtonsoft library. This library provides a JsonConvert class which can be used to deserialize a JSON object into a list. The DeserializeObject method of the JsonConvert class takes a string of JSON data as an argument and returns a list of objects.

##### Section 4: How to Deserialize a JSON Object into a List?
To deserialize a JSON object into a list, you need to use the DeserializeObject method of the JsonConvert class. This method takes a string of JSON data as an argument and returns a list of objects. The list can then be used to access the data stored in the JSON object.
