---
title: A single property has multiple names assigned to it using jsonproperty
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: No, it is not possible to assign multiple JsonProperty names to a single property.
---

**Contents**

[TOC]

## Section 1: Is it possible?
Yes, it is possible to assign multiple JsonProperty names to a single property.

## Section 2: How to do it?
The JsonProperty attribute can be used to specify the name of the property when it is serialized to JSON. This can be done by providing an array of strings to the Name property of the JsonProperty attribute.

## Section 3: Example
For example, consider the following model class:
```
public class Person
{
    [JsonProperty(Name = new string[] { "FirstName", "GivenName" })]
    public string FirstName { get; set; }
}
```
In this example, the FirstName property will be serialized to JSON with both the name "FirstName" and "GivenName".

## Section 4: Benefits
This feature can be useful when integrating with third-party APIs that use different naming conventions. It can also be used to provide backward compatibility when changing the names of properties in a model class.
