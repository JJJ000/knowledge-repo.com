---
title: How to ignore a field when performing .net JSON serialization, similar to [xmlignore]?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The [JsonIgnore] attribute can be used to ignore a field during .NET JSON serialization.
---

**Contents**

[TOC]

1. Using the `[JsonIgnore]` Attribute 

The `[JsonIgnore]` attribute lets you specify that a property should be ignored when the object is serialized to JSON. The following code example shows how to use the `[JsonIgnore]` attribute to ignore the `IsAdmin` property when the object is serialized to JSON.

```
public class User
{
    public string Name { get; set; }
    public string Email { get; set; }

    [JsonIgnore]
    public bool IsAdmin { get; set; }
}
```

2. Using the `JsonSerializerSettings` Class 

The `JsonSerializerSettings` class allows you to configure a number of settings when serializing an object to JSON. You can use this class to ignore a property when serializing an object to JSON. The following code example shows how to use the `JsonSerializerSettings` class to ignore the `IsAdmin` property when the object is serialized to JSON.

```
public class User
{
    public string Name { get; set; }
    public string Email { get; set; }
    public bool IsAdmin { get; set; }
}

var user = new User { Name = "John Doe", Email = "john@example.com", IsAdmin = true };

var settings = new JsonSerializerSettings
{
    ContractResolver = new DefaultContractResolver
    {
        IgnoreSerializableAttribute = true,
        IgnoreSerializableInterface = true,
        NamingStrategy = new DefaultNamingStrategy
        {
            IgnoreProperties = new HashSet<string> { "IsAdmin" }
        }
    }
};

var json = JsonConvert.SerializeObject(user, settings);
```

3. Using the `JsonConverter` Class 

The `JsonConverter` class allows you to customize the serialization process. You can use this class to ignore a property when serializing an object to JSON. The following code example shows how to use the `JsonConverter` class to ignore the `IsAdmin` property when the object is serialized to JSON.

```
public class User
{
    public string Name { get; set; }
    public string Email { get; set; }
    public bool IsAdmin { get; set; }
}

public class UserConverter : JsonConverter
{
    public override bool CanConvert(Type objectType)
    {
        return objectType == typeof(User);
    }

    public override void WriteJson(JsonWriter writer, object value, JsonSerializer serializer)
    {
        var user = (User)value;
        writer.WriteStartObject();
        writer.WritePropertyName("Name");
        serializer.Serialize(writer, user.Name);
        writer.WritePropertyName("Email");
        serializer.Serialize(writer, user.Email);
        writer.WriteEndObject();
    }

    public override object ReadJson(JsonReader reader, Type objectType, object existingValue, JsonSerializer serializer)
    {
        throw new NotImplementedException();
    }
}

var user = new User { Name = "John Doe", Email = "john@example.com", IsAdmin = true };

var settings = new JsonSerializerSettings
{
    Converters = new List<JsonConverter> { new UserConverter() }
};

var json = JsonConvert.SerializeObject(user, settings);
```
