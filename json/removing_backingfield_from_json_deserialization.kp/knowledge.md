---
title: How can I exclude the k__backingfield property when deserializing json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the [JsonProperty] attribute to specify the name of the property when serializing and deserializing.
---

**Contents**

[TOC]

## Section 1: Understand the Problem
When deserializing JSON, the k__BackingField is a field that appears in the output. This field is a representation of a private variable that is used by the compiler to store the value of a property.

## Section 2: Identify the Solution
The solution to this problem is to use a custom JsonConverter when deserializing the JSON. This will allow you to write custom logic to remove the k__BackingField from the output.

## Section 3: Implement the Solution
The following code sample shows how to implement a custom JsonConverter to remove the k__BackingField from the output when deserializing JSON.

```
public class MyJsonConverter : JsonConverter
{
    public override bool CanConvert(Type objectType)
    {
        return true;
    }

    public override object ReadJson(JsonReader reader, Type objectType, object existingValue, JsonSerializer serializer)
    {
        JObject jo = JObject.Load(reader);
        jo.Descendants().OfType<JProperty>()
            .Where(p => p.Name.StartsWith("k__BackingField"))
            .ToList()
            .ForEach(p => p.Remove());

        return jo.ToObject(objectType);
    }

    public override void WriteJson(JsonWriter writer, object value, JsonSerializer serializer)
    {
        JToken t = JToken.FromObject(value);
        t.WriteTo(writer);
    }
}
```

## Section 4: Use the Solution
Once you have implemented the custom JsonConverter, you can use it when deserializing the JSON. The following code sample shows how to use the custom JsonConverter when deserializing the JSON.

```
string json = "{\"k__BackingField\":\"value\"}";
MyObject obj = JsonConvert.DeserializeObject<MyObject>(json, new MyJsonConverter());
```
