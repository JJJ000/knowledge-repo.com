---
title: Making sure JSON keys are in lowercase in .net
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the Newtonsoft.Json library to deserialize JSON into a JObject and then use the JObject.ToObject<T>() method to convert it into a strongly-typed object with all keys lowercase.
---

**Contents**

[TOC]

1. Using Json.NET 
    - Json.NET is a popular library for working with JSON in .NET. It provides a number of methods to ensure json keys are lowercase, including:
    - `JsonSerializerSettings.ContractResolver` - allows you to specify a custom contract resolver to modify the way json is serialized and deserialized.
    - `JsonConvert.SerializeObject` - allows you to specify a custom serializer settings object when serializing objects to JSON.

2. Using LINQ to JSON 
    - LINQ to JSON is a library for working with JSON in .NET. It provides a number of methods to ensure json keys are lowercase, including:
    - `JObject.Parse` - allows you to parse a JSON string into a JObject and then use LINQ to iterate through the keys and modify them as needed.
    - `JObject.ToString` - allows you to serialize a JObject back to a JSON string with the keys modified as needed.

3. Using Regular Expressions 
    - Regular expressions can be used to search and replace JSON keys with lowercase versions. This can be done by searching for any uppercase characters in the JSON string and replacing them with their lowercase version.

4. Manual Method 
    - The manual method involves manually iterating through the JSON object and replacing any uppercase keys with their lowercase version. This approach can be time consuming and error-prone, so it is not recommended for large or complex objects.
