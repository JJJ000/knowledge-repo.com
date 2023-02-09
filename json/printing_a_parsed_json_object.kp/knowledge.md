---
title: What does the parsed JSON object look like when printed?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The JSON parsed object can be printed in JSON format by using the JSON.stringify() method.
---

**Contents**

[TOC]

## Section 1: Parsing a JSON Object

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to exchange data between different applications. It is a text-based format and is designed to be easily readable by both humans and machines. To parse a JSON object, you need to use a JSON parser, which is a software library that can interpret a JSON string and convert it into a native data structure.

## Section 2: Printing a JSON Object

Once you have parsed a JSON object, you can print it out in its original format. To do this, you need to use a JSON encoder, which is a software library that can take a native data structure and convert it into a JSON string. This string can then be printed out or saved to a file.

## Section 3: Using Python to Parse and Print a JSON Object

Python is a popular programming language that has a built-in JSON module which makes it easy to parse and print JSON objects. To parse a JSON object in Python, you can use the json.loads() function. To print a JSON object, you can use the json.dumps() function.

## Section 4: Example of Parsing and Printing a JSON Object in Python

Below is an example of how to parse and print a JSON object in Python:

```
import json

# Parse JSON string
json_string = '{"name": "John Doe", "age": 30}'
data = json.loads(json_string)

# Print JSON string
print(json.dumps(data))
```

The output of this code would be:

```
{"name": "John Doe", "age": 30}
```
