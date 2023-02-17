---
title: Convert deep objects to JSON strings
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: JSON.stringify can be used to convert deep objects into JSON strings.
---

**Contents**

[TOC]

# Section 1: Overview

JSON.stringify is a JavaScript function that converts a JavaScript object or value to a JSON string. This function is typically used when sending data from a client to a server, as the JSON format is a common format for data interchange.

# Section 2: Deep Objects

When a JavaScript object contains nested objects, or objects that contain other objects, the JSON.stringify() function will convert those nested objects into strings as well. This is referred to as stringifying deep objects.

# Section 3: Syntax

The syntax for stringifying deep objects is similar to the syntax for stringifying regular objects. The only difference is that the objects must be nested within each other.

# Section 4: Example

For example, if we have an object that contains a nested object, we can use the following syntax to stringify it:

```
let myObj = {
    name: 'John',
    age: 25,
    address: {
        street: '123 Main St.',
        city: 'Los Angeles',
        state: 'CA'
    }
};

let myObjString = JSON.stringify(myObj);
```

The resulting string will look like this:

```
{"name":"John","age":25,"address":{"street":"123 Main St.","city":"Los Angeles","state":"CA"}}
```
