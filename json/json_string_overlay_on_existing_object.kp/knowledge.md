---
title: Apply data from a JSON string on top of an already existing object instance
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use a library like Jackson or Gson to deserialize the JSON string and map it to the existing object instance.
---

**Contents**

[TOC]

## Parsing the JSON String

The first step in overlaying data from a JSON string onto an existing object instance is to parse the JSON string. This can be done using the `JSON.parse()` method, which takes a JSON string as its argument and returns a JavaScript object.

```javascript
const jsonString = '{"name":"John Smith","age":30,"city":"New York"}';
const json = JSON.parse(jsonString);
```

## Merging Objects

The next step is to merge the existing object instance with the parsed JSON object. This can be done using the `Object.assign()` method, which takes one or more objects as its arguments and merges them into a single object. The first argument to `Object.assign()` is the target object, and the subsequent arguments are the source objects.

```javascript
const obj = {name: "Jane Smith", address: "123 Main St", age: 25};
Object.assign(obj, json);
```

In this example, the `json` object is merged into the `obj` object, overwriting any properties that have the same name.

## Updating Existing Properties

If the JSON string contains properties that already exist in the target object, those properties will be overwritten by the corresponding values in the JSON object. However, if you want to preserve the existing values and only update certain properties, you can manually update those properties after merging the objects.

```javascript
const obj = {name: "Jane Smith", address: "123 Main St", age: 25};
const json = {name: "John Smith", age: 30, city: "New York"};
const merged = Object.assign(obj, json);

if (json.name) {
  merged.name = json.name;
}
```

In this example, the `name` property is updated with the value from the JSON object only if it exists in the JSON object.
