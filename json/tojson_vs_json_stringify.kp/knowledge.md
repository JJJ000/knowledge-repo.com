---
title: What distinguishes tojson() from json.stringify()?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: toJSON() is a method that is used to customize the JSON string, while JSON.stringify() is a method that converts an object or value to a JSON string.
---

**Contents**

[TOC]

# What is JSON?
JSON stands for JavaScript Object Notation. It is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. JSON is a text format that is completely language independent but uses conventions that are familiar to programmers of the C family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others.

## toJSON()
The `toJSON()` method is used to convert a JavaScript object into a JSON string. It is a built-in method of the JavaScript `Object` class. This method is called when the object is being serialized to JSON. It is essentially a callback function that can modify the behavior of the JSON serialization process.

### Syntax
```javascript
object.toJSON(key)
```

### Parameters
- `key` (optional) - A string representing the key of the object property being serialized.

### Return Value
The `toJSON()` method returns the JSON representation of the object.

## JSON.stringify()
The `JSON.stringify()` method is used to convert a JavaScript object into a JSON string. It is a built-in method of the `JSON` object. This method is used to convert a JavaScript object into a JSON string that can be transmitted or stored in a file.

### Syntax
```javascript
JSON.stringify(value[, replacer[, space]])
```

### Parameters
- `value` - The value to be converted into a JSON string.
- `replacer` (optional) - A function that alters the behavior of the stringification process or an array of strings and numbers that serve as a whitelist for selecting the properties of the object to be included in the JSON string.
- `space` (optional) - A string or number that's used to insert whitespace into the output JSON string for readability purposes.

### Return Value
The `JSON.stringify()` method returns a JSON string representing the value. 

## Difference between toJSON() and JSON.stringify()
The main difference between `toJSON()` and `JSON.stringify()` is that `toJSON()` is a method that is called on an object during serialization that allows for custom serialization logic, while `JSON.stringify()` is a standalone function that converts a JavaScript object to a JSON string.

The `toJSON()` method is used to customize the serialization behavior of an object. When an object is stringified with `JSON.stringify()`, it checks if the object has a `toJSON()` method. If the object has a `toJSON()` method, it is called to return the JSON value that should be serialized. If the object does not have a `toJSON()` method, the default serialization behavior is used.

In contrast, `JSON.stringify()` is a generic function that can be used to convert any JavaScript object into a JSON string. It does not require the object to have a `toJSON()` method. `JSON.stringify()` can also take additional parameters that customize its behavior, such as a `replacer` function that can filter, transform, or selectively serialize object properties or an optional `space` parameter that can add indentation or line breaks to the output string to improve readability. 

In summary, `toJSON()` is a method that can be used to customize the serialization behavior of an object, while `JSON.stringify()` is a standalone function that can be used to convert any JavaScript object into a JSON string.
