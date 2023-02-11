---
title: What is the best way to deal with null or empty values when using jsonconvert.deserializeobject?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The JsonConvert.DeserializeObject method will ignore null/empty values by default.
---

**Contents**

[TOC]

#### Option 1: Ignore Null Values

Using the `NullValueHandling` property of the `JsonSerializerSettings` class, you can specify how the `JsonConvert.DeserializeObject` method should handle null values. The `Ignore` setting will cause the `JsonConvert.DeserializeObject` method to ignore any null values in the JSON string.

```csharp
var jsonString = "{ 'Name': 'John', 'Age': null }";

var settings = new JsonSerializerSettings
{
    NullValueHandling = NullValueHandling.Ignore
};

var person = JsonConvert.DeserializeObject<Person>(jsonString, settings);
```

#### Option 2: Replace Null Values

Using the `DefaultValueHandling` property of the `JsonSerializerSettings` class, you can specify how the `JsonConvert.DeserializeObject` method should handle null values. The `Replace` setting will cause the `JsonConvert.DeserializeObject` method to replace any null values in the JSON string with the default value of the property type.

```csharp
var jsonString = "{ 'Name': 'John', 'Age': null }";

var settings = new JsonSerializerSettings
{
    DefaultValueHandling = DefaultValueHandling.Replace
};

var person = JsonConvert.DeserializeObject<Person>(jsonString, settings);
```

#### Option 3: Throw an Exception

Using the `MissingMemberHandling` property of the `JsonSerializerSettings` class, you can specify how the `JsonConvert.DeserializeObject` method should handle null values. The `Error` setting will cause the `JsonConvert.DeserializeObject` method to throw an exception if any null values are encountered in the JSON string.

```csharp
var jsonString = "{ 'Name': 'John', 'Age': null }";

var settings = new JsonSerializerSettings
{
    MissingMemberHandling = MissingMemberHandling.Error
};

var person = JsonConvert.DeserializeObject<Person>(jsonString, settings);
```

#### Option 4: Deserialize as Nullable Types

Using the `TypeNameHandling` property of the `JsonSerializerSettings` class, you can specify how the `JsonConvert.DeserializeObject` method should handle null values. The `Objects` setting will cause the `JsonConvert.DeserializeObject` method to deserialize any null values in the JSON string as nullable types.

```csharp
var jsonString = "{ 'Name': 'John', 'Age': null }";

var settings = new JsonSerializerSettings
{
    TypeNameHandling = TypeNameHandling.Objects
};

var person = JsonConvert.DeserializeObject<Person>(jsonString, settings);
```
