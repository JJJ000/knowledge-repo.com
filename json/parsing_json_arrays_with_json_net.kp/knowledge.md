---
title: Processing a JSON array with json.net
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Json.Net can be used to parse a JSON array by deserializing it into a corresponding .NET type.
---

**Contents**

[TOC]

### Section 1: Deserializing a JSON Array

JSON.NET provides the `JsonConvert.DeserializeObject<T>` method to deserialize a JSON array into a .NET type. The type `T` can be either a `List<T>` or an array of `T`.

### Section 2: Example

Let's say we have the following JSON array:

```
[
  {
    "name": "John",
    "age": 30
  },
  {
    "name": "Jane",
    "age": 25
  }
]
```

We can deserialize it into a `List<Person>` using the following code:

```csharp
List<Person> people = JsonConvert.DeserializeObject<List<Person>>(json);
```

Where `Person` is a class defined as follows:

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
```

### Section 3: Deserializing to an Array

If you need to deserialize the JSON array into an array of `Person`, you can use the following code:

```csharp
Person[] people = JsonConvert.DeserializeObject<Person[]>(json);
```

### Section 4: Error Handling

It is important to note that if the JSON array contains invalid data, the deserialization will fail with an exception. It is therefore important to catch any exceptions and handle them appropriately.
