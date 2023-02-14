---
title: Looping through a JSON object in c#
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: You can iterate over a JSON object in C# using the Newtonsoft.Json library`s JObject.Parse() method.
---

**Contents**

[TOC]

### Section 1 - Deserializing JSON String

The first step in iterating over a JSON object in C# is to deserialize the JSON string into an object. This can be done using the JavaScriptSerializer class, which is part of the System.Web.Script.Serialization namespace.

```csharp
string jsonString = "{"key1": "value1", "key2": "value2"}";
JavaScriptSerializer serializer = new JavaScriptSerializer();
Dictionary<string, object> deserializedJSON = serializer.Deserialize<Dictionary<string, object>>(jsonString);
```

### Section 2 - Iterating Over the Deserialized JSON

Once the JSON string has been deserialized, it can be iterated over using a foreach loop.

```csharp
foreach (KeyValuePair<string, object> kvp in deserializedJSON)
{
    string key = kvp.Key;
    object value = kvp.Value;
    // Do something with the key and value
}
```

### Section 3 - Accessing Nested JSON Objects

If the JSON string contains nested objects, they can be accessed using the dynamic keyword.

```csharp
foreach (KeyValuePair<string, object> kvp in deserializedJSON)
{
    string key = kvp.Key;
    dynamic value = kvp.Value;
    if (value is Dictionary<string, object>)
    {
        // Nested JSON object
        foreach (KeyValuePair<string, object> nestedKvp in value)
        {
            string nestedKey = nestedKvp.Key;
            object nestedValue = nestedKvp.Value;
            // Do something with the nested key and value
        }
    }
    else
    {
        // Not a nested JSON object
        // Do something with the key and value
    }
}
```

### Section 4 - Deserializing to a Strongly Typed Object

If the JSON string is known to have a specific structure, it can be deserialized to a strongly typed object. This can be done using the DataContractJsonSerializer class, which is part of the System.Runtime.Serialization namespace.

```csharp
string jsonString = "{"key1": "value1", "key2": "value2"}";
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(jsonString));
DataContractJsonSerializer serializer = new DataContractJsonSerializer(typeof(MyObject));
MyObject deserializedObject = (MyObject)serializer.ReadObject(stream);
```

Once the object has been deserialized, it can be iterated over using a foreach loop.

```csharp
foreach (PropertyInfo property in deserializedObject.GetType().GetProperties())
{
    string key = property.Name;
    object value = property.GetValue(deserializedObject);
    // Do something with the key and value
}
```
