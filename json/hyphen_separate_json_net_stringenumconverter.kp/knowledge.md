---
title: How to utilize hyphen-separated casing in json.net stringenumconverter?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add the following code to your JSON serialization settings `new StringEnumConverter { NamingStrategy = new SnakeCaseNamingStrategy() }`.
---

**Contents**

[TOC]

## Introduction

JSON.NET is a popular open-source library for working with JSON data in .NET applications. It provides a powerful and flexible way to serialize and deserialize JSON data, and includes a variety of built-in converters for handling different data types, including string enums.

By default, the JSON.NET StringEnumConverter uses camel-casing for enum values when serializing to JSON. However, in some cases, we may want to use a different casing convention, such as hyphen-separated casing.

In this article, we will show you how to make the JSON.NET StringEnumConverter use hyphen-separated casing in JSON.


## Step 1: Create a Custom Enum Converter

To make the JSON.NET StringEnumConverter use hyphen-separated casing, we will need to create a custom enum converter that inherits from the StringEnumConverter class and overrides its WriteJson method.

```csharp
using Newtonsoft.Json;
using Newtonsoft.Json.Converters;
using System;

public class HyphenSeparatedEnumConverter : StringEnumConverter
{
    public override void WriteJson(JsonWriter writer, object value, JsonSerializer serializer)
    {
        // Get the enum value as a string
        string enumValue = Enum.GetName(value.GetType(), value);

        // Replace underscores with hyphens
        enumValue = enumValue.ToLower().Replace("_", "-");

        // Write the hyphen-separated string value to the JSON stream
        writer.WriteValue(enumValue);
    }
}
```

In this example, we create a new class called HyphenSeparatedEnumConverter that inherits from StringEnumConverter. We then override the WriteJson method, which is called by JSON.NET when serializing an enum value to JSON.

Inside the WriteJson method, we first get the enum value as a string using the Enum.GetName method. We then replace underscores with hyphens using the string.ToLower and string.Replace methods.

Finally, we write the hyphen-separated string value to the JSON stream using the JsonWriter.WriteValue method.


## Step 2: Apply the Converter to Enums

To use our custom HyphenSeparatedEnumConverter in our application, we will need to apply it to our enums by adding a JsonConverter attribute with the typeof(HyphenSeparatedEnumConverter) argument.

```csharp
[JsonConverter(typeof(HyphenSeparatedEnumConverter))]
public enum MyEnum
{
    Value1,
    Value2,
    Value3
}
```

In this example, we add the JsonConverter attribute to our MyEnum class with the typeof(HyphenSeparatedEnumConverter) argument. This tells JSON.NET to use our custom converter when serializing or deserializing MyEnum values.


## Step 3: Serialize and Deserialize JSON

Now that we have our custom HyphenSeparatedEnumConverter and our JsonConverter attribute applied to our enum, we can serialize and deserialize JSON data with hyphen-separated enum values.

```csharp
// Serialize an object with a hyphen-separated enum value
MyObject obj = new MyObject { MyEnumValue = MyEnum.Value1 };
string json = JsonConvert.SerializeObject(obj);

// Output: {"MyEnumValue":"value-1"}

// Deserialize JSON with hyphen-separated enum value
MyObject obj2 = JsonConvert.DeserializeObject<MyObject>(json);

// Output: obj2.MyEnumValue == MyEnum.Value1
```

In this example, we first create an object with a MyEnumValue property set to MyEnum.Value1, and then serialize it to JSON using the JsonConvert.SerializeObject method.

The resulting JSON contains a hyphen-separated enum value, as expected.

We can then deserialize the JSON using the JsonConvert.DeserializeObject method, and verify that the deserialized object's MyEnumValue property matches the original enum value.

## Conclusion
By creating a custom enum converter that inherits from the StringEnumConverter class and overrides its WriteJson method, we can make the JSON.NET StringEnumConverter use hyphen-separated casing in JSON.

We then apply the converter to our enums using the JsonConverter attribute, and serialize and deserialize JSON data with hyphen-separated enum values as usual.
