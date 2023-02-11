---
title: Extracting key/value pairs from a JSON response using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The JSON.parse() method can be used to parse a JSON string and get the key/value pairs.
---

**Contents**

[TOC]

**Section 1: What is JSON?**

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is a text-based format that is easy for humans to read and write. It is also easy for machines to parse and generate.

**Section 2: Parsing JSON in JavaScript**

JSON can be parsed in JavaScript using the JSON.parse() method. This method takes a string of JSON data and returns a JavaScript object. For example, the following code parses a JSON string and returns a JavaScript object:

```
var jsonData = '{"name": "John", "age": 25}';
var data = JSON.parse(jsonData);
```

**Section 3: Accessing JSON Key/Value Pairs**

Once the JSON string has been parsed into a JavaScript object, the key/value pairs can be accessed using the dot notation or bracket notation. For example, the following code accesses the name and age values from the JSON string:

```
var name = data.name; // returns "John"
var age = data['age']; // returns 25
```

**Section 4: Iterating Over JSON Key/Value Pairs**

The JavaScript for...in loop can be used to iterate over all the keys in a JSON object. The following example shows how to loop through the key/value pairs and print out the values:

```
for (var key in data) {
  console.log(data[key]);
}
```

The output of the code would be:

```
John
25
```
