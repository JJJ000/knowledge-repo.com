---
title: Does the list/array conform to the JSON standard?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: No, a list/array is not valid JSON; it must be a key-value pair in the form of an object.
---

**Contents**

[TOC]

## Definition of JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used for storing and exchanging information. It is a text-based, human-readable format that is used to represent data in a structured way.

## Is a List/Array Valid JSON?

Yes, a list/array can be valid JSON. A JSON array is an ordered collection of values, which are enclosed within square brackets. Each value is separated by a comma. The values can be strings, numbers, objects, arrays, and boolean values, or any combination of these data types. 

## Example of a Valid JSON Array

Below is an example of a valid JSON array:

```
[
    "Apple",
    "Banana",
    "Orange"
]
```

## How to Validate JSON

To validate JSON, you can use online tools such as JSONLint. This tool will check your JSON code for any syntax errors and will let you know if it is valid or not.
