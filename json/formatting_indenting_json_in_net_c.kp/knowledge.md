---
title: What is the best way to format and indent JSON in .net using c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the JsonSerializerSettings class to configure the JSON serialization settings such as formatting and indentation.
---

**Contents**

[TOC]

## Serialize an Object

To get formatted and indented JSON in .NET using C#, you can serialize an object using the `Newtonsoft.Json` library. First, you will need to add a reference to the library in your project.

Then, you can create an instance of the `JsonSerializerSettings` class and set the `Formatting` property to `Formatting.Indented` to get the formatted and indented JSON.

```csharp
JsonSerializerSettings settings = new JsonSerializerSettings();
settings.Formatting = Formatting.Indented;
```

## Serialize the Object

Once the settings are configured, you can use the `JsonConvert.SerializeObject` method to serialize the object.

```csharp
string json = JsonConvert.SerializeObject(myObject, settings);
```

## Output the JSON

Finally, you can output the JSON string to a file or the console.

```csharp
Console.WriteLine(json);
```
