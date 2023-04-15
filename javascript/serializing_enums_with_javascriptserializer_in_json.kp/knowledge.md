---
title: Can JavaScriptSerializer convert an enumerated type to a json string?
authors:
- cool_wizard
tags:
- javascript
- json
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, the JavaScriptSerializer can serialize an enum as a string in JSON.
---

**Contents**

[TOC]

### Overview
JavaScriptSerializer is a .NET class library that enables developers to serialize and deserialize objects into and from JSON format. It is part of the .NET Framework and is included in the System.Web.Script.Serialization namespace. It allows developers to convert objects into a JSON string and vice versa.

### Enum Serialization
When serializing an enum with JavaScriptSerializer, the enum will be serialized as a string. This means that when the serialized JSON is deserialized back into an enum, the string value will be used to create the enum instead of the underlying integer value.

### Usage
To use JavaScriptSerializer to serialize and deserialize objects, you must first create an instance of the JavaScriptSerializer class. Then, you can use the Serialize and Deserialize methods to convert objects into and from JSON strings.

### Example
For example, if you have an enum declared like this:

```javascript
public enum MyEnum
{
    Value1,
    Value2
}
```

You can serialize it to a JSON string like this:

```javascript
var serializer = new JavaScriptSerializer();
string jsonString = serializer.Serialize(MyEnum.Value1);
```

The resulting JSON string will be:

```javascript
"Value1"
```

And you can deserialize it back to the enum like this:

```javascript
MyEnum value = serializer.Deserialize<MyEnum>(jsonString);
```
