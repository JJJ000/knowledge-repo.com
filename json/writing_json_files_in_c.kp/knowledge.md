---
title: What is the process for creating a JSON file using c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Create a JObject or JArray object, populate it with data, and then serialize it to a string and save it to a file.
---

**Contents**

[TOC]

### 1. Create JSON Object

To begin writing a JSON file in C#, you must first create a JSON object. The JSON object can be created using the Newtonsoft.Json library. This library can be installed using the NuGet package manager.

```c#
using Newtonsoft.Json;

dynamic jsonObject = new JObject();
```

### 2. Add Data to JSON Object

Once the JSON object has been created, data can be added to it. This can be done by adding properties and values to the object.

```c#
jsonObject.name = "John";
jsonObject.age = 25;
```

### 3. Serialize JSON Object

Once the JSON object has been populated with data, it must be serialized. This can be done using the Newtonsoft.Json library.

```c#
string jsonString = JsonConvert.SerializeObject(jsonObject);
```

### 4. Write JSON to File

Finally, the serialized JSON object can be written to a file. This can be done using the System.IO library.

```c#
using (StreamWriter file = File.CreateText("data.json"))
{
    file.Write(jsonString);
}
```
