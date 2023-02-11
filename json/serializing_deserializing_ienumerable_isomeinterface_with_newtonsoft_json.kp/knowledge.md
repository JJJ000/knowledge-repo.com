---
title: Serialize and deserialize a class with a property of type ienumerable<isomeinterface> using newtonsoft.json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: NewtonSoft.Json can serialize and deserialize classes with properties of type IEnumerable<ISomeInterface> by marking the interface with the [JsonObject] attribute.
---

**Contents**

[TOC]

### Serializing

To serialize a class with a property of type `IEnumerable<ISomeInterface>`, we can use the `JsonConvert` class from the NewtonSoft.Json library. The `JsonConvert` class has a static `SerializeObject` method which takes an object and returns a JSON string representation of the object.

The following example shows how to use the `JsonConvert` class to serialize a class with a property of type `IEnumerable<ISomeInterface>`:

```csharp
public class MyClass
{
    public IEnumerable<ISomeInterface> MyProperty { get; set; }
}

// Create an instance of MyClass
var myClass = new MyClass { MyProperty = new List<ISomeInterface>() };

// Serialize the instance of MyClass
string json = JsonConvert.SerializeObject(myClass);
```

### Deserializing

To deserialize a JSON string into a class with a property of type `IEnumerable<ISomeInterface>`, we can also use the `JsonConvert` class from the NewtonSoft.Json library. The `JsonConvert` class has a static `DeserializeObject` method which takes a JSON string and returns an object of the specified type.

The following example shows how to use the `JsonConvert` class to deserialize a JSON string into a class with a property of type `IEnumerable<ISomeInterface>`:

```csharp
public class MyClass
{
    public IEnumerable<ISomeInterface> MyProperty { get; set; }
}

// Create a JSON string representing an instance of MyClass
string json = "{\"MyProperty\": []}";

// Deserialize the JSON string into an instance of MyClass
MyClass myClass = JsonConvert.DeserializeObject<MyClass>(json);
```
