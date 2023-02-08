---
title: What is the opposite of json.stringify?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The reverse of JSON.stringify is JSON.parse, which converts a JSON string into a JavaScript object.
---

**Contents**

[TOC]

### JSON.parse

JSON.parse() is a method used to convert a JSON string into a JavaScript object. The syntax for the method is: 

`JSON.parse(string)`

Where string is the JSON string to be parsed. The method returns the JavaScript object created from the JSON string.

### Example

Let's look at an example of JSON.parse() in action.

Suppose we have the following JSON string:

`'{"name": "John Doe", "age": 30}'`

We can use JSON.parse() to convert this string into a JavaScript object:

```
let obj = JSON.parse('{"name": "John Doe", "age": 30}');

console.log(obj); // {name: "John Doe", age: 30}
```

### Limitations

JSON.parse() only works with valid JSON strings. If the string is not valid JSON, the method will throw an error.

### Security

It's important to note that JSON.parse() should only be used on trusted data. If the string being parsed is not trusted, it could contain malicious code, which could be executed when parsed.
