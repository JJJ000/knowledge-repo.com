---
title: Including "null" in json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: It is not possible to send NaN in JSON since it does not support the NaN value type.
---

**Contents**

[TOC]

#Solution

##Stringify NaN
The most common way to send NaN in JSON is to use the `JSON.stringify()` method. This will convert the NaN value into a string, which can be sent as part of a JSON string.

##JSON.stringify()
The `JSON.stringify()` method takes a JavaScript object and converts it into a JSON string. It will convert any values that are not valid JSON, such as NaN, into strings.

##Examples
For example, if you have a JavaScript object with a `value` property that contains a NaN value, you can use `JSON.stringify()` to convert it into a JSON string:

```
const obj = {
  value: NaN
};
const jsonStr = JSON.stringify(obj);
console.log(jsonStr); // {"value":"NaN"}
```

##Limitations
One potential limitation of this approach is that it will only work for valid JSON values. If you have a value that is not valid JSON, such as a function or a symbol, then `JSON.stringify()` will not be able to convert it into a JSON string.
