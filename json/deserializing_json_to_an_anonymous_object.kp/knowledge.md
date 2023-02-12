---
title: Convert JSON into an anonymous object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Deserializing JSON to an anonymous object can be done by using the JsonConvert.DeserializeObject method.
---

**Contents**

[TOC]

# Deserialize JSON

To deserialize JSON, you can use the `JSON.parse()` function in JavaScript. This function takes a string of JSON data and returns an anonymous object.

# Syntax

The syntax for `JSON.parse()` is as follows:

`JSON.parse(text[, reviver])`

Where `text` is the string of JSON data and `reviver` is an optional parameter that can be used to transform the data before it is returned. 

# Example

For example, the following JSON string:

`{"name": "John", "age": 30}`

Can be deserialized using the `JSON.parse()` function as follows:

```
let jsonString = '{"name": "John", "age": 30}';
let obj = JSON.parse(jsonString);
console.log(obj);
// Output: {name: "John", age: 30}
```

# Reviver Parameter

The `reviver` parameter is an optional parameter that can be used to transform the data before it is returned. It takes a function that is called for each property in the JSON string and can be used to modify the data before it is returned.

For example, the following code will convert all property values to upper case before returning the object:

```
let jsonString = '{"name": "John", "age": 30}';
let obj = JSON.parse(jsonString, (key, value) => {
  return typeof value === "string" ? value.toUpperCase() : value;
});
console.log(obj);
// Output: {name: "JOHN", age: 30}
```
