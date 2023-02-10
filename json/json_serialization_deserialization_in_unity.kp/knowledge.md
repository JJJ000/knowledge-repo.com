---
title: Convert JSON and JSON array into a format that can be stored in unity, then convert it back into its original form
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Unity provides the JsonUtility class to serialize and deserialize Json and Json Array.
---

**Contents**

[TOC]

#### Serializing Json in Unity

To serialize a json object in Unity, you can use the `JsonUtility` class to convert a json string into an object. The `JsonUtility` class provides two methods: `ToJson` and `FromJson`. The `ToJson` method takes an object and returns a json string. The `FromJson` method takes a json string and returns an object. 

For example, to serialize a `Person` class into a json string:

```csharp
public class Person {
    public string name;
    public int age;
    public List<string> hobbies;
}

Person person = new Person { name = "John", age = 20, hobbies = new List<string> { "reading", "swimming" } };

string jsonString = JsonUtility.ToJson(person);
```

The `jsonString` variable will contain the following json string:

```json
{
  "name": "John",
  "age": 20,
  "hobbies": [
    "reading",
    "swimming"
  ]
}
```

#### Deserializing Json in Unity

To deserialize a json string in Unity, you can use the `JsonUtility` class to convert a json string into an object. The `JsonUtility` class provides two methods: `ToJson` and `FromJson`. The `ToJson` method takes an object and returns a json string. The `FromJson` method takes a json string and returns an object. 

For example, to deserialize a json string into a `Person` class:

```csharp
public class Person {
    public string name;
    public int age;
    public List<string> hobbies;
}

string jsonString = "{\"name\":\"John\",\"age\":20,\"hobbies\":[\"reading\",\"swimming\"]}";

Person person = JsonUtility.FromJson<Person>(jsonString);
```

The `person` variable will contain the following `Person` object:

```csharp
Person person = new Person { name = "John", age = 20, hobbies = new List<string> { "reading", "swimming" } };
```

#### Serializing Json Array in Unity

To serialize a json array in Unity, you can use the `JsonUtility` class to convert an array of objects into a json string. The `JsonUtility` class provides two methods: `ToJson` and `FromJson`. The `ToJson` method takes an object and returns a json string. The `FromJson` method takes a json string and returns an object. 

For example, to serialize an array of `Person` objects into a json string:

```csharp
public class Person {
    public string name;
    public int age;
    public List<string> hobbies;
}

Person[] people = new Person[] { 
    new Person { name = "John", age = 20, hobbies = new List<string> { "reading", "swimming" } },
    new Person { name = "Jane", age = 22, hobbies = new List<string> { "painting", "cooking" } }
};

string jsonString = JsonUtility.ToJson(people);
```

The `jsonString` variable will contain the following json string:

```json
[
  {
    "name": "John",
    "age": 20,
    "hobbies": [
      "reading",
      "swimming"
    ]
  },
  {
    "name": "Jane",
    "age": 22,
    "hobbies": [
      "painting",
      "cooking"
    ]
  }
]
```

#### Deserializing Json Array in Unity

To deserialize a json array in Unity, you can use the `JsonUtility` class to convert a json string into an array of objects. The `JsonUtility` class provides two methods: `ToJson` and `FromJson`. The `ToJson` method takes an object and returns a json string. The `FromJson` method takes a json string and returns an object. 

For example, to deserialize a json string into an array of `Person` objects:

```csharp
public class Person {
