---
title: The difference between json.stringify and json.parse is that json.stringify converts a JavaScript object into a JSON string, while json.parse takes a JSON string and converts it into a JavaScript object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: JSON.stringify converts a JavaScript object into a JSON string, whereas JSON.parse converts a JSON string into a JavaScript object.
---

**Contents**

[TOC]

**JSON.stringify()**

- **Purpose**: The JSON.stringify() method converts a JavaScript object or value to a JSON string.

- **Syntax**: JSON.stringify(value[, replacer[, space]]) 

- **Parameters**: 
  - value: The value to convert to a JSON string.
  - replacer: Optional. A function that alters the behavior of the stringification process, or an array of String and Number objects that serve as a whitelist for selecting/filtering the properties of the value object to be included in the JSON string.
  - space: Optional. A String or Number object that's used to insert white space into the output JSON string for readability purposes.

**JSON.parse()**

- **Purpose**: The JSON.parse() method parses a JSON string, constructing the JavaScript value or object described by the string.

- **Syntax**: JSON.parse(text[, reviver])

- **Parameters**: 
  - text: The string to parse as JSON.
  - reviver: Optional. A function that transforms the results. This function is called for each member of the object. If a member contains nested objects, the nested objects are transformed before the parent object is.
