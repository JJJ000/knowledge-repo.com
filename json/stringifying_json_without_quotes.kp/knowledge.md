---
title: Stringify a JSON object without including quotation marks around the property names
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON.stringify does not allow for properties to be without quotes.
---

**Contents**

[TOC]

# Solution 1

Using ES6 Syntax:

```javascript
const myObj = {
  name: "John Doe",
  age: 28
};

JSON.stringify(myObj, (key, value) => {
  if (typeof value === 'string') return value;
  return value;
});
```

# Solution 2

Using Object.keys():

```javascript
const myObj = {
  name: "John Doe",
  age: 28
};

const keys = Object.keys(myObj);

let str = "{";

for (let i = 0; i < keys.length; i++) {
  str += keys[i] + ":" + myObj[keys[i]];
  if (i < keys.length - 1) str += ",";
}

str += "}";

JSON.stringify(str);
```
