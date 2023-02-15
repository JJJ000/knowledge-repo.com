---
title: Changing the datetime display in ASP.NET core 3.0 with system.text.json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the JsonSerializerOptions.Converters collection to add a custom JsonConverter to format DateTime objects.
---

**Contents**

[TOC]

## Setting Up the DateTime Format

The DateTime format can be set up using the `JsonSerializerOptions` class. When instantiating the class, the `DateTimeFormat` property should be set to the desired format string.

```C#
var options = new JsonSerializerOptions
{
    DateTimeFormat = "yyyy-MM-dd HH:mm:ss"
};
```

## Serializing DateTime

Once the `JsonSerializerOptions` have been set up, the DateTime can be serialized using the `JsonSerializer.Serialize` method.

```C#
var dateTime = DateTime.Now;
var json = JsonSerializer.Serialize(dateTime, options);
```

## Deserializing DateTime

The DateTime can be deserialized using the `JsonSerializer.Deserialize` method.

```C#
var dateTime = JsonSerializer.Deserialize<DateTime>(json, options);
```

## Using the DateTimeFormat Attribute

The DateTime format can also be specified using the `JsonConverter` attribute. This allows for the DateTime format to be set on a per-property basis.

```C#
public class MyClass
{
    [JsonConverter(typeof(DateTimeFormatConverter), "yyyy-MM-dd HH:mm:ss")]
    public DateTime DateTime { get; set; }
}
```
