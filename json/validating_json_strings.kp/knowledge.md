---
title: Verifying if a string is valid JSON before attempting to parse it?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can use the JSON.parse() function to check if a string is valid JSON.
---

**Contents**

[TOC]

1. Using Regular Expressions
    Regular expressions can be used to check if a string is valid json. The expression `^[\],:{}\s]*$` can be used to check if the characters in the string are valid json characters. If the expression returns true, then the string is valid json.

2. Using the JSON.parse() Method
    The JSON.parse() method can be used to check if a string is valid json. The method will return an error if the string is not valid json, otherwise it will return the parsed json object.

3. Using the JSONLint Library
    The JSONLint library can be used to check if a string is valid json. The library will return an error if the string is not valid json, otherwise it will return the parsed json object.

4. Using the JSON Schema
    The JSON Schema can be used to check if a string is valid json. The schema is a set of rules that define what a valid json object should look like. If the string does not match the rules in the schema, then it is not valid json.
