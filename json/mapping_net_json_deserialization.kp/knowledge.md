---
title: Rename the property of a .net newtonsoft JSON deserialized object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, it is possible to map a property name in JSON to a different property name when deserializing using NewtonSoft JSON by using the JsonProperty attribute.
---

**Contents**

[TOC]

#### Option 1: Using JsonProperty Attribute 
The JsonPropertyAttribute can be used to change the name of the property when it is serialized to JSON.

Example:
```csharp
public class Person
{
    [JsonProperty("full_name")]
    public string Name { get; set; }
}
```

#### Option 2: Using JsonConverter
The JsonConverter can be used to customize the deserialization process.

Example:
```csharp
public class Person
{
    public string Name { get; set; }

    [JsonConverter(typeof(MyJsonConverter))]
    public string FullName { get; set; }
}

public class MyJsonConverter : JsonConverter
{
    public override bool CanConvert(Type objectType)
    {
        return objectType == typeof(string);
    }

    public override object ReadJson(JsonReader reader, Type objectType, object existingValue, JsonSerializer serializer)
    {
        JObject jo = JObject.Load(reader);
        return jo["full_name"].ToString();
    }

    public override void WriteJson(JsonWriter writer, object value, JsonSerializer serializer)
    {
        throw new NotImplementedException();
    }
}
```

#### Option 3: Using Custom Contract Resolver
The DefaultContractResolver can be used to customize the property mapping.

Example:
```csharp
public class Person
{
    public string Name { get; set; }
}

public class MyContractResolver : DefaultContractResolver
{
    protected override string ResolvePropertyName(string propertyName)
    {
        if (propertyName == "Name")
        {
            return "full_name";
        }
        return propertyName;
    }
}

var settings = new JsonSerializerSettings
{
    ContractResolver = new MyContractResolver()
};

string json = JsonConvert.SerializeObject(person, settings);
```

#### Option 4: Using JsonSerializerSettings
The JsonSerializerSettings can be used to customize the property mapping.

Example:
```csharp
public class Person
{
    public string Name { get; set; }
}

var settings = new JsonSerializerSettings
{
    ContractResolver = new DictionaryContractResolver(new Dictionary<string, string>
    {
        { "Name", "full_name" }
    })
};

string json = JsonConvert.SerializeObject(person, settings);
```
