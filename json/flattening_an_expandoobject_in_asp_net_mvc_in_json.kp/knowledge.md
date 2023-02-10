---
title: What is the best way to convert an expandoobject returned from a jsonresult in ASP.NET mvc to a flat structure?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `dynamic` keyword to access the properties of the ExpandoObject and flatten them into a dictionary.
---

**Contents**

[TOC]

# Section 1: Understanding ExpandoObject
ExpandoObject is a .NET dynamic object that allows properties to be added and removed at run time. It is a useful object for working with dynamic data, such as data returned from a web service, or data stored in a database.

# Section 2: Flattening an ExpandoObject
An ExpandoObject can be flattened into a dictionary using the `ToDictionary` method. This method takes an `IDictionary<string, object>` and returns a flattened dictionary of the ExpandoObject's properties.

# Section 3: Using the Dictionary
Once the ExpandoObject is flattened, the resulting dictionary can be used to access the data within the ExpandoObject. The dictionary can be looped through to access each property and its value, or the values can be accessed directly using the property name as the dictionary key.

# Section 4: Example
Here is an example of how to flatten an ExpandoObject and access its properties:

```
var expandoObject = new ExpandoObject();
expandoObject.Name = "John";
expandoObject.Age = 20;

// Flatten the ExpandoObject
var dictionary = expandoObject.ToDictionary();

// Access the properties
var name = dictionary["Name"];
var age = dictionary["Age"];
```
