---
title: Process JSON data using c#
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can parse JSON in C# using the Newtonsoft.Json library.
---

**Contents**

[TOC]

## Parsing JSON with Newtonsoft.Json

The Newtonsoft.Json library provides an easy-to-use API for parsing JSON in C#. To parse JSON, you need to create a JsonSerializerSettings object and pass it to the JsonConvert.DeserializeObject() method.

```
JsonSerializerSettings settings = new JsonSerializerSettings();
MyObject obj = JsonConvert.DeserializeObject<MyObject>(jsonString, settings);
```

## Parsing JSON with System.Text.Json

The System.Text.Json library provides an easy-to-use API for parsing JSON in C#. To parse JSON, you need to create a JsonSerializerOptions object and pass it to the JsonSerializer.Deserialize() method.

```
JsonSerializerOptions options = new JsonSerializerOptions();
MyObject obj = JsonSerializer.Deserialize<MyObject>(jsonString, options);
```

## Parsing JSON with JavaScriptSerializer

The JavaScriptSerializer class provides an easy-to-use API for parsing JSON in C#. To parse JSON, you need to create a JavaScriptSerializer object and pass it to the Deserialize() method.

```
JavaScriptSerializer serializer = new JavaScriptSerializer();
MyObject obj = serializer.Deserialize<MyObject>(jsonString);
```

## Parsing JSON with DataContractJsonSerializer

The DataContractJsonSerializer class provides an easy-to-use API for parsing JSON in C#. To parse JSON, you need to create a DataContractJsonSerializer object and pass it to the ReadObject() method.

```
DataContractJsonSerializer serializer = new DataContractJsonSerializer(typeof(MyObject));
MyObject obj = (MyObject)serializer.ReadObject(jsonString);
```
