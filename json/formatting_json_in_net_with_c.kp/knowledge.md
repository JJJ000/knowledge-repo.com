---
title: What is the most efficient way to format JSON in .net using c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the Newtonsoft.Json library to serialize and format JSON in .NET using C#.
---

**Contents**

[TOC]

1. Using Newtonsoft.Json
---------------------------------
Using the Newtonsoft.Json library, you can use the JsonConvert.SerializeObject() method to get formatted JSON from a .NET object. This method takes a .NET object as an argument and returns a string representation of the JSON object.

2. Using System.Text.Json
---------------------------------
Using the System.Text.Json library, you can use the JsonSerializer.Serialize() method to get formatted JSON from a .NET object. This method takes a .NET object as an argument and returns a string representation of the JSON object.

3. Configuring the Serialization
---------------------------------
You can configure the serialization options of both Newtonsoft.Json and System.Text.Json to get the desired formatting of the JSON output. This can be done by creating a JsonSerializerSettings object and passing it to the serialization method.

4. Using PrettyPrint
---------------------------------
You can also use the PrettyPrint extension method provided by the Newtonsoft.Json library to get a formatted JSON output. This method takes a string representation of a JSON object as an argument and returns a string representation of the formatted JSON object.
