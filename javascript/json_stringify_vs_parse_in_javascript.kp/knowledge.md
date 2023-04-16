---
title: The difference between json.stringify and json.parse is that json.stringify converts a JavaScript object into a JSON string, while json.parse converts a JSON string into a JavaScript object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JSON.stringify converts a JavaScript object into a JSON string, while JSON.parse converts a JSON string into a JavaScript object.
---

**Contents**

[TOC]

### JSON.stringify
JSON.stringify() is a method in JavaScript that converts a JavaScript object into a JSON string. It can take two parameters: the object to convert to a string, and an optional replacer function which can be used to filter or modify the data before it is stringified.

### JSON.parse
JSON.parse() is a method in JavaScript that takes a JSON string and parses it into a JavaScript object. It can take two parameters: the JSON string to parse, and an optional reviver function which can be used to filter or modify the data before it is parsed.

### Difference
The main difference between JSON.stringify and JSON.parse is that JSON.stringify is used to convert a JavaScript object into a JSON string, while JSON.parse is used to convert a JSON string into a JavaScript object.
