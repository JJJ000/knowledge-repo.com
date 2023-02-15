---
title: Is it possible to specify a route in an attribute to connect a property in my class to a nested property in my json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: Yes, you can use the JsonProperty attribute to specify a path to map a property in your class to a child property in your JSON.
---

**Contents**

[TOC]

**Section 1: What is JSON?**

JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging data between different systems. It is based on a subset of the JavaScript programming language and is used to structure data in a way that is easy for humans to read and write.

**Section 2: What is an Attribute?**

An attribute is a piece of data associated with an object. In JSON, attributes are used to represent the properties of an object. They can be used to map a property in a class to a child property in a JSON object.

**Section 3: How to Specify a Path in an Attribute**

When specifying a path in an attribute, you need to provide the full path to the property you want to map. This can include the name of the parent object, the name of the child object, and any intermediate objects. For example, if you wanted to map a property in a class to a property in a JSON object called "person" that had a child object called "address", the path would be "person.address".

**Section 4: Example**

For example, if you had a class called "Person" with a property called "name" and a JSON object with a child object called "address" that had a property called "street", you could use an attribute to map the "name" property in the class to the "street" property in the JSON object like this:

```
[JsonProperty("person.address.street")]
public string Name { get; set; }
```
