---
title: Constructing a JSON array in c#
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: A JSON array in C# can be created using the JsonConvert.SerializeObject() method.
---

**Contents**

[TOC]

**Section 1: Create a C# Class**

First, create a C# class that will represent the JSON array. This class should have properties that represent the data in the array. For example, if the array contains objects of type Person, the class should have properties such as Name, Age, and Email.

```csharp
public class Person 
{
    public string Name { get; set; }
    public int Age { get; set; }
    public string Email { get; set; }
}
```

**Section 2: Create a List of the Class**

Next, create a list of the class created in the previous step. This list will contain the data that will be serialized into the JSON array.

```csharp
List<Person> people = new List<Person>();
people.Add(new Person{ Name = "John Doe", Age = 30, Email = "john@example.com" });
people.Add(new Person{ Name = "Jane Doe", Age = 25, Email = "jane@example.com" });
```

**Section 3: Serialize the List**

Now, serialize the list of objects into a JSON string using the Newtonsoft.Json library.

```csharp
string jsonArray = JsonConvert.SerializeObject(people);
```

**Section 4: Output the JSON Array**

Finally, output the JSON array to the console.

```csharp
Console.WriteLine(jsonArray);
```
