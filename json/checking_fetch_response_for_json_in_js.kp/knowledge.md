---
title: How to determine if the result of a fetch request is a JSON object in javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Check if the response of a fetch is a JSON object by using the `response.json()` method.
---

**Contents**

[TOC]

#### 1. Parse the Response

The first step to check if the response of a fetch is a JSON object is to parse the response into a JavaScript object. This can be done using the `JSON.parse()` method. 

```javascript
let response = await fetch(url);
let data = await response.json();
let jsonObject = JSON.parse(data);
```

#### 2. Check the Type

Once the response has been parsed, the next step is to check the type of the object. This can be done using the `typeof` operator.

```javascript
if (typeof jsonObject === 'object') {
  console.log('The response is a JSON object');
} else {
  console.log('The response is not a JSON object');
}
```

#### 3. Check Properties

Another way to check if the response is a JSON object is to check the properties of the object. JSON objects have a `__proto__` property which can be used to verify the type of the object.

```javascript
if (jsonObject.__proto__ === Object.prototype) {
  console.log('The response is a JSON object');
} else {
  console.log('The response is not a JSON object');
}
```

#### 4. Use a Library

Finally, there are libraries available which can be used to check if the response is a JSON object. One such library is `is-json`.

```javascript
const isJSON = require('is-json');

if (isJSON(jsonObject)) {
  console.log('The response is a JSON object');
} else {
  console.log('The response is not a JSON object');
}
```
