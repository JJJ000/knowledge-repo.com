---
title: Is it possible to use linq with json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, LINQ can be used to query JSON data in C#.
---

**Contents**

[TOC]

Yes, you can LINQ a JSON in C# using the Newtonsoft.Json library. Here are the steps to do it:

### 1. Install Newtonsoft.Json package

To use LINQ with JSON, we need to install the Newtonsoft.Json package using NuGet package manager.

### 2. Create JSON data

Suppose we have a JSON data as follows:

```json
{
   "employees": [
      {
         "firstName": "John",
         "lastName": "Doe",
         "age": 30
      },
      {
         "firstName": "Jane",
         "lastName": "Doe",
         "age": 25
      },
      {
         "firstName": "Jim",
         "lastName": "Smith",
         "age": 40
      }
   ]
}
```

We can store this data in a string variable or can read from a file or web API using the `HttpClient` class.

### 3. Parse JSON to C# object

The `JsonConvert` class of the Newtonsoft.Json library provides a method `DeserializeObject` to convert a JSON string to a C# object.

```csharp
string json = "{...}"; // JSON data
var data = JsonConvert.DeserializeObject(json);
```

We can also use a class to deserialize the JSON to a strongly-typed object.

```csharp
public class Employee
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public int Age { get; set; }
}

public class RootObject
{
    public List<Employee> Employees { get; set; }
}

string json = "{...}"; // JSON data
var data = JsonConvert.DeserializeObject<RootObject>(json);
```

### 4. Query the JSON using LINQ

Once we have the C# object, we can use LINQ to query the JSON data.

```csharp
// Get all employees with age greater than 25
var result = data.Employees.Where(e => e.Age > 25).ToList();

// Group employees by last name
var groups = data.Employees.GroupBy(e => e.LastName)
                           .Select(g => new {
                               LastName = g.Key,
                               Count = g.Count(),
                               AverageAge = g.Average(e => e.Age)
                           }).ToList();
```

The `result` variable will contain a list of employees with age greater than 25. The `groups` variable will contain a list of objects with last name, count, and average age of employees for each group.

These are the basic steps to LINQ a JSON in C#.
