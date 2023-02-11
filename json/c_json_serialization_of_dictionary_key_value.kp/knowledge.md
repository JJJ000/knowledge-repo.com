---
title: Serializing a c# dictionary into JSON as {keyvalue, ...} instead of {keykey, valuevalue, ...}
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the JsonProperty attribute to customize the serialization of a Dictionary.
---

**Contents**

[TOC]

## Using JsonProperty

You can use the [JsonProperty](https://www.newtonsoft.com/json/help/html/T_Newtonsoft_Json_JsonPropertyAttribute.htm) attribute to customize the serialization of a `Dictionary` object into JSON. This can be used to serialize the object into a `{key:value, ...}` format.

For example, if you have a `Dictionary<string, string>` object, you can use the `JsonProperty` attribute to customize the serialization of the object like this:

```csharp
public class MyDictionary
{
    [JsonProperty(PropertyName = "key")]
    public Dictionary<string, string> MyDictionary { get; set; }
}
```

## Using Custom JsonConverter

You can also create a custom `JsonConverter` to serialize a `Dictionary` object into a `{key:value, ...}` format.

To do this, you need to override the `WriteJson` method of the `JsonConverter` class and write custom logic to serialize the `Dictionary` object into the desired format.

For example, if you have a `Dictionary<string, string>` object, you can create a `JsonConverter` like this:

```csharp
public class MyDictionaryConverter : JsonConverter
{
    public override void WriteJson(JsonWriter writer, object value, JsonSerializer serializer)
    {
        var dict = (Dictionary<string, string>)value;

        writer.WriteStartObject();
        foreach (var kvp in dict)
        {
            writer.WritePropertyName(kvp.Key);
            writer.WriteValue(kvp.Value);
        }
        writer.WriteEndObject();
    }

    public override bool CanConvert(Type objectType)
    {
        return objectType == typeof(Dictionary<string, string>);
    }
}
```

## Using Custom Serializer

Finally, you can also create a custom serializer to serialize a `Dictionary` object into a `{key:value, ...}` format.

To do this, you need to create a custom serializer class that implements the `ISerializer` interface and override the `Serialize` method.

For example, if you have a `Dictionary<string, string>` object, you can create a custom serializer like this:

```csharp
public class MyDictionarySerializer : ISerializer
{
    public string Serialize(object obj)
    {
        var dict = (Dictionary<string, string>)obj;

        var sb = new StringBuilder();
        sb.Append("{");
        foreach (var kvp in dict)
        {
            sb.AppendFormat("\"{0}\":\"{1}\",", kvp.Key, kvp.Value);
        }
        sb.Remove(sb.Length - 1, 1);
        sb.Append("}");

        return sb.ToString();
    }
}
```
