---
title: How to exclude the __type property when serializing JSON objects
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the [JsonIgnore] attribute on the \_\_type property to prevent it from being serialized.
---

**Contents**

[TOC]

## Using the IgnoreDataMember Attribute

The `IgnoreDataMember` attribute can be used to prevent the `__type` property from being serialized when using the `DataContractJsonSerializer` class. This attribute can be applied to the type that is being serialized, as well as to any properties that should not be serialized. For example:

```csharp
[DataContract]
public class MyType
{
    [DataMember]
    public string Name { get; set; }

    [IgnoreDataMember]
    public int __type { get; set; }
}
```

## Using the JsonIgnore Attribute

The `JsonIgnore` attribute can be used to prevent the `__type` property from being serialized when using the `Newtonsoft.Json` library. This attribute can be applied to the type that is being serialized, as well as to any properties that should not be serialized. For example:

```csharp
public class MyType
{
    [JsonProperty]
    public string Name { get; set; }

    [JsonIgnore]
    public int __type { get; set; }
}
```

## Using the JsonSerializerSettings

The `JsonSerializerSettings` class can also be used to prevent the `__type` property from being serialized. This class has a `ContractResolver` property that can be used to specify a custom `IContractResolver` implementation that can be used to ignore the `__type` property. For example:

```csharp
public class MyType
{
    public string Name { get; set; }
    public int __type { get; set; }
}

// ...

var jsonSettings = new JsonSerializerSettings
{
    ContractResolver = new MyTypeContractResolver()
};

var json = JsonConvert.SerializeObject(myType, jsonSettings);
```

```csharp
public class MyTypeContractResolver : DefaultContractResolver
{
    protected override IList<JsonProperty> CreateProperties(Type type, MemberSerialization memberSerialization)
    {
        var props = type.GetProperties()
            .Where(p => p.Name != "__type")
            .Select(p => base.CreateProperty(p, memberSerialization))
            .Union(type.GetFields().Select(f => base.CreateProperty(f, memberSerialization)))
            .ToList();

        props.ForEach(p => { p.Writable = true; p.Readable = true; });

        return props;
    }
}
```
