---
title: Converting a JSON string into a c# poco class using jsonconvert.deserializeobject
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: JsonConvert.DeserializeObject can be used to deserialize a JSON string into a C# POCO class.
---

**Contents**

[TOC]

**Section 1: Overview**

JsonConvert.DeserializeObject is a method in the Newtonsoft.Json library that can be used to deserialize JSON into a C# POCO (Plain Old CLR Object) class. This method takes a JSON string and a type, and then returns the deserialized object.

**Section 2: Setup**

The first step in using JsonConvert.DeserializeObject is to add the Newtonsoft.Json library to your project. This can be done by either installing it via NuGet or by downloading it from the Newtonsoft website.

**Section 3: Usage**

Once the library is installed, the next step is to create a POCO class to use with the deserialization. This class should have the same structure as the JSON string that is being deserialized. Once the class is created, the JsonConvert.DeserializeObject method can be used to deserialize the JSON string. This method takes two parameters: the JSON string and the type of the POCO class.

**Section 4: Example**

Here is an example of how to use the JsonConvert.DeserializeObject method.

//Create a POCO class
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}

//Create a JSON string
string jsonString = "{\"Name\":\"John\",\"Age\":25}";

//Deserialize the JSON string
Person person = JsonConvert.DeserializeObject<Person>(jsonString);
