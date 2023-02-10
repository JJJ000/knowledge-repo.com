---
title: Retrieving the identifier of a jtoken using json.net
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JToken.Path property to get the name/key of a JToken.
---

**Contents**

[TOC]

##### Section 1: Using JsonPropertyAttribute

The simplest way to get the name / key of a JToken using JSON.net is to use the JsonPropertyAttribute. This attribute can be applied to a property of a class, and it will be used to define the name of the property when it is serialized or deserialized.

For example, if you have a class like this:

```
public class MyClass
{
    [JsonProperty("myKey")]
    public string MyValue { get; set; }
}
```

You can then serialize an instance of this class to a JToken and get the name of the property by using the JsonPropertyAttribute:

```
MyClass myObject = new MyClass();
JToken token = JToken.FromObject(myObject);
string key = token["myKey"].ToString();
```

##### Section 2: Using LINQ

Another way to get the name / key of a JToken using JSON.net is to use LINQ. This can be done by using the JObject.Property method, which returns a JProperty object. This object contains the name of the property, which can then be accessed using the Name property.

For example, if you have a JToken like this:

```
JToken token = JToken.Parse("{\"myKey\": \"myValue\"}");
```

You can then get the name of the property by using the JObject.Property method:

```
string key = ((JProperty)token.SelectToken("$")).Name;
```

##### Section 3: Using the Dictionary

The final way to get the name / key of a JToken using JSON.net is to use a Dictionary. This can be done by converting the JToken to a Dictionary, and then accessing the key of the desired property.

For example, if you have a JToken like this:

```
JToken token = JToken.Parse("{\"myKey\": \"myValue\"}");
```

You can then convert it to a Dictionary and access the key of the desired property:

```
Dictionary<string, object> dict = token.ToObject<Dictionary<string, object>>();
string key = dict.Keys.First();
```
