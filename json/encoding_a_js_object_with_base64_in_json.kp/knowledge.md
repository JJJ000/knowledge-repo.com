---
title: Encode a JavaScript object using base64
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The JavaScript object can be Base64 encoded by stringifying the object and then using the btoa() method.
---

**Contents**

[TOC]

**Section 1: Encoding JSON Object**

To encode a JavaScript object in JSON, we first need to convert it to a string. This can be done using the `JSON.stringify()` function.

```javascript
let myObject = {
  name: 'John Smith',
  age: 34
};

let myObjectString = JSON.stringify(myObject);
```

**Section 2: Encoding String to Base64**

Once we have the string representation of the object, we can encode it to Base64 using the `btoa()` function.

```javascript
let myObjectBase64 = btoa(myObjectString);
```

**Section 3: Decoding Base64**

To decode the Base64 encoded string, we can use the `atob()` function.

```javascript
let myObjectStringDecoded = atob(myObjectBase64);
```

**Section 4: Decoding JSON Object**

Finally, we can decode the JSON object from the string using the `JSON.parse()` function.

```javascript
let myObjectDecoded = JSON.parse(myObjectStringDecoded);
```
