---
title: What is the best way to work with a single item and an array for the same property when using json.net?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JsonPropertyAttribute`s ItemConverterType to specify a JsonConverter to handle both a single item and an array for the same property.
---

**Contents**

[TOC]

## Deserializing Single Item

When deserializing a single item, the property should be declared as a single object. This can be done by defining the property as an object type in the class definition.

For example, if the JSON contains a single item for the property `myProperty`, the class definition should be as follows:

```C#
public class MyClass
{
    public MyObject myProperty { get; set; }
}
```

Then, when using JSON.NET to deserialize the JSON, the property will be deserialized as a single object.

## Deserializing Array

When deserializing an array, the property should be declared as an array type in the class definition. This can be done by defining the property as an array type, for example `List<MyObject>`.

For example, if the JSON contains an array for the property `myProperty`, the class definition should be as follows:

```C#
public class MyClass
{
    public List<MyObject> myProperty { get; set; }
}
```

Then, when using JSON.NET to deserialize the JSON, the property will be deserialized as an array.

## Handling Both Single Item and Array

When handling both single item and array for the same property, the property should be declared as an `object` type in the class definition. This allows the property to be deserialized as either a single object or an array, depending on the structure of the JSON.

For example, if the JSON contains either a single item or an array for the property `myProperty`, the class definition should be as follows:

```C#
public class MyClass
{
    public object myProperty { get; set; }
}
```

Then, when using JSON.NET to deserialize the JSON, the property will be deserialized as either a single object or an array, depending on the structure of the JSON.

## Checking Property Type

When handling both single item and array for the same property, it is also possible to check the type of the property after deserialization. This can be done by using the `GetType()` method to check the type of the property.

For example, if the JSON contains either a single item or an array for the property `myProperty`, the following code can be used to check the type of the property:

```C#
if (myProperty.GetType() == typeof(MyObject))
{
    // Property is a single item
}
else if (myProperty.GetType() == typeof(List<MyObject>))
{
    // Property is an array
}
```
