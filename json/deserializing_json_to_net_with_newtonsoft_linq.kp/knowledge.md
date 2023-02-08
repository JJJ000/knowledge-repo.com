---
title: Using newtonsoft or linq to JSON to convert a JSON string into a .net object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Newtonsoft`s Json.NET library can be used to deserialize JSON into .NET objects.
---

**Contents**

[TOC]

### Section 1: Install Newtonsoft

To use Newtonsoft for deserializing JSON to .NET objects, you must first install the Newtonsoft package. This can be done through the NuGet package manager.

### Section 2: Create the .NET Object

Create a .NET object that has the same structure as the JSON. This object will be used to store the deserialized JSON.

### Section 3: Deserialize the JSON

Using the Newtonsoft library, deserialize the JSON into the .NET object. This can be done using the JsonConvert.DeserializeObject method.

### Section 4: Access the Deserialized Data

Once the JSON has been deserialized, you can access the data in the .NET object. This can be done by accessing the properties of the object.
