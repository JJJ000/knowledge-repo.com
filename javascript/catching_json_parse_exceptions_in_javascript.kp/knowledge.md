---
title: What is the correct way to handle errors when using json.parse?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Catch the SyntaxError thrown by JSON.parse in a try-catch block.
---

**Contents**

[TOC]

##### Try/Catch Block

The most common way to catch an exception from `JSON.parse()` is to use a `try/catch` block. This allows you to handle any errors that may occur during the parsing process.

```javascript
try {
  const data = JSON.parse(jsonString);
  // Do something with the parsed data
} catch (e) {
  // Handle any errors that occurred during parsing
}
```

##### Error Callback

Another way to catch an exception from `JSON.parse()` is to use an error callback. This allows you to handle any errors that may occur during the parsing process.

```javascript
JSON.parse(jsonString, (err, data) => {
  if (err) {
    // Handle any errors that occurred during parsing
  } else {
    // Do something with the parsed data
  }
});
```

##### Return Value

The return value of `JSON.parse()` can also be used to detect any errors that may occur during the parsing process. If an error occurs, `JSON.parse()` will return `null`.

```javascript
const data = JSON.parse(jsonString);
if (data === null) {
  // Handle any errors that occurred during parsing
} else {
  // Do something with the parsed data
}
```
