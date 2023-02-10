---
title: Transform a JSON object into a buffer and then back into a JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: To convert a JSON Object to a Buffer, use the Buffer.from() method; to convert a Buffer back to a JSON Object, use the JSON.parse() method.
---

**Contents**

[TOC]

## Converting a JSON Object to Buffer

A Buffer can be created from a JSON object by using the `Buffer.from` method. This method takes in a JSON string as an argument and returns a Buffer object with the contents of the JSON object.

Example: 

```javascript
const jsonObject = {
  name: 'John',
  age: 30
};

const buffer = Buffer.from(JSON.stringify(jsonObject));
```

## Converting a Buffer to a JSON Object

A JSON object can be created from a Buffer by using the `Buffer.toString` method. This method takes in the Buffer object as an argument and returns a JSON string. This JSON string can then be parsed using the `JSON.parse` method to convert it into a JSON object.

Example: 

```javascript
const jsonString = buffer.toString();
const jsonObject = JSON.parse(jsonString);
```

## Conclusion

In conclusion, a JSON object can be converted to a Buffer object and back to a JSON object using the `Buffer.from` and `Buffer.toString` methods respectively.
