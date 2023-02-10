---
title: What is the best way to loop through a jobject?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Loop through the JObject`s Properties collection to enumerate its contents.
---

**Contents**

[TOC]

1. Accessing JObject Properties

To access the properties of a JObject, you can use the `GetValue` method on the `JObject` instance. This method takes the name of the property you wish to access as a parameter. For example:

```
var myJObject = JObject.Parse("{\"Name\": \"John Doe\"}");
var name = myJObject.GetValue("Name");
```

2. Enumerating JObject Properties

To enumerate through the properties of a JObject, you can use the `Properties` method. This method returns an `IEnumerable<JProperty>` which can then be enumerated through. For example:

```
var myJObject = JObject.Parse("{\"Name\": \"John Doe\", \"Age\": 30}");

foreach (var property in myJObject.Properties())
{
    Console.WriteLine($"{property.Name}: {property.Value}");
}
```

This will output the following:

```
Name: John Doe
Age: 30
```

3. Accessing Nested Properties

To access nested properties of a JObject, you can use the `SelectToken` method. This method takes a string representing the path to the desired property. For example:

```
var myJObject = JObject.Parse("{\"Person\": {\"Name\": \"John Doe\", \"Age\": 30}}");

var name = myJObject.SelectToken("Person.Name");
```

4. Enumerating Nested Properties

To enumerate through nested properties of a JObject, you can use the `SelectTokens` method. This method takes a string representing the path to the desired properties, and returns an `IEnumerable<JToken>` which can then be enumerated through. For example:

```
var myJObject = JObject.Parse("{\"Person\": {\"Name\": \"John Doe\", \"Age\": 30}}");

foreach (var token in myJObject.SelectTokens("Person.*"))
{
    Console.WriteLine($"{token.Path}: {token.Value}");
}
```

This will output the following:

```
Person.Name: John Doe
Person.Age: 30
```
