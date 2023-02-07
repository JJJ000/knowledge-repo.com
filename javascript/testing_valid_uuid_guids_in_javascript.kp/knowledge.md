---
title: What is the procedure for verifying a uuid/guid?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the built-in RegExp object to test if a string is a valid UUID/GUID.
---

**Contents**

[TOC]

## Using Regular Expressions

Regular expressions are a great way to test for valid UUIDs/GUIDs in JavaScript. The following is a regular expression that can be used to test for valid UUIDs/GUIDs:

```js
/^[0-9a-f]{8}-[0-9a-f]{4}-[1-5][0-9a-f]{3}-[89ab][0-9a-f]{3}-[0-9a-f]{12}$/i
```

This regular expression can be used with the `test()` method of a JavaScript `RegExp` object to test for valid UUIDs/GUIDs. The following is an example of how this can be used:

```js
let regex = /^[0-9a-f]{8}-[0-9a-f]{4}-[1-5][0-9a-f]{3}-[89ab][0-9a-f]{3}-[0-9a-f]{12}$/i;
let uuid = '12345678-1234-5678-abcd-1234567890ab';

if (regex.test(uuid)) {
  console.log('Valid UUID/GUID!');
} else {
  console.log('Invalid UUID/GUID!');
}
```

## Using Libraries

There are also libraries available to help with validating UUIDs/GUIDs in JavaScript. A popular library for this purpose is [uuid-validate](https://www.npmjs.com/package/uuid-validate). This library provides a `validate()` function that can be used to test for valid UUIDs/GUIDs. The following is an example of how this can be used:

```js
let uuid = require('uuid-validate');
let uuidString = '12345678-1234-5678-abcd-1234567890ab';

if (uuid.validate(uuidString)) {
  console.log('Valid UUID/GUID!');
} else {
  console.log('Invalid UUID/GUID!');
}
```
