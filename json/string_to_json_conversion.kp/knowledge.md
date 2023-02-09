---
title: Transforming a string into a JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: A string can be converted to a JSON object using the JSON.parse() method.
---

**Contents**

[TOC]

## Section 1: What is JSON?
JSON stands for JavaScript Object Notation. It is a lightweight data-interchange format that is used to store and exchange data between two systems. It is an open standard format that is both human-readable and machine-readable.

## Section 2: Converting a String to a JSON Object
A string can be converted to a JSON object using the `JSON.parse()` method. This method takes a string as an argument and parses it into a JavaScript object.

## Section 3: Example
For example, the following string can be converted to a JSON object: 

```
var string = '{"name":"John","age":30,"city":"New York"}';

var jsonObject = JSON.parse(string);
```

## Section 4: Output
The output of the above code will be a JSON object that looks like this:

```
{
  "name": "John",
  "age": 30,
  "city": "New York"
}
```
