---
title: Serialize an object using json.net and specify a root name
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Json.NET allows for serializing an object with a root name by using the JsonSerializerSettings and setting the ContractResolver property to a custom DefaultContractResolver.
---

**Contents**

[TOC]

# Section 1: Serialize Object with Root Name

Json.NET can be used to serialize an object with a root name. This can be done by setting the JsonSerializerSettings.RootPropertyName property to the desired root name.

# Section 2: Using RootPropertyName

To use the RootPropertyName property, an instance of the JsonSerializerSettings class must be created and configured. The RootPropertyName property must be set to the desired root name.

# Section 3: Serializing an Object

Once the JsonSerializerSettings instance is configured, the object can be serialized by passing the object and the JsonSerializerSettings instance to the JsonConvert.SerializeObject() method. The result will be a string containing the serialized object with the root name set in the JsonSerializerSettings instance.

# Section 4: Example

For example, consider the following Person class:

```
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
```

To serialize an instance of the Person class with a root name of "PersonData", the following code can be used:

```
Person person = new Person { Name = "John Doe", Age = 42 };

JsonSerializerSettings settings = new JsonSerializerSettings { RootPropertyName = "PersonData" };

string json = JsonConvert.SerializeObject(person, settings);

// json = {"PersonData":{"Name":"John Doe","Age":42}}
```
