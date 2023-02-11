---
title: What is the best way to extract values from a JSON string using c#?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the Newtonsoft.Json library to deserialize the JSON string into an object and access the values.
---

**Contents**

[TOC]

## Section 1: Deserialize the JSON

The first step is to deserialize the JSON string into an object. This can be done using the `JsonConvert` class in the `Newtonsoft.Json` package.

```c#
string json = "{\"key1\":\"value1\", \"key2\":\"value2\"}";

// Deserialize the JSON string
var values = JsonConvert.DeserializeObject<Dictionary<string, string>>(json);
```

## Section 2: Access the Values

Once the JSON string has been deserialized, the values can be accessed using the keys.

```c#
// Access the values
string value1 = values["key1"];
string value2 = values["key2"];
```

## Section 3: Iterate Over the Values

It is also possible to iterate over the values in the dictionary.

```c#
// Iterate over the values
foreach (var kvp in values)
{
    Console.WriteLine($"{kvp.Key}: {kvp.Value}");
}
```

## Section 4: Serialize the Values

Finally, the values can be serialized back into a JSON string using the `JsonConvert` class.

```c#
// Serialize the values
string json = JsonConvert.SerializeObject(values);
```
