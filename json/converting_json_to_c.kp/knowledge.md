---
title: Transform JSON string into c# object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The JSON string can be deserialized into a C# object using the Newtonsoft.Json library.
---

**Contents**

[TOC]

## Deserializing a JSON String

The first step in converting a JSON string to a C# object is to deserialize the string. The easiest way to do this is to use the `JsonConvert.DeserializeObject()` method from the Newtonsoft.Json library. This method takes a JSON string as a parameter and returns an object of type `dynamic`.

## Creating a Class

The next step is to create a C# class that matches the structure of the JSON string. This class should have properties that match the names of the keys in the JSON string, and the types of the properties should match the types of the values in the JSON string.

## Mapping the Object

Once the class has been created, the `JsonConvert.DeserializeObject()` method can be used again to map the JSON string to the newly created class. This method takes two parameters: the JSON string and the type of the class.

## Deserializing the Object

The final step is to deserialize the object. This can be done using the `JsonConvert.DeserializeObject()` method, passing in the object and the type of the class. This will return an instance of the class, populated with the data from the JSON string.
