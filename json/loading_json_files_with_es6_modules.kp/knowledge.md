---
title: What is the process for loading a JSON file using an es6 module?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Import a JSON file using the `import` statement, followed by the path to the JSON file.
---

**Contents**

[TOC]

### Using Fetch

ES6 modules allow us to use the `fetch` API to load a JSON file. This is done by using the `fetch` method, which takes the URL of the JSON file as the first argument and returns a `Promise` object.

```js
fetch('path/to/file.json')
  .then(response => response.json())
  .then(data => {
    // do something with the data
  });
```

### Using XMLHttpRequest

Another way to load a JSON file using ES6 modules is to use the `XMLHttpRequest` object. This is done by creating a new `XMLHttpRequest` object and setting the `responseType` to `"json"`.

```js
const xhr = new XMLHttpRequest();
xhr.open('GET', 'path/to/file.json', true);
xhr.responseType = 'json';
xhr.onload = function () {
  if (xhr.status === 200) {
    const data = xhr.response;
    // do something with the data
  }
};
xhr.send();
```

### Using Node.js

If you are using Node.js, you can use the `fs` module to read the JSON file. This is done by using the `readFile` method, which takes the path to the file as the first argument and a callback function as the second argument. The callback function will be called with the contents of the file as the first argument.

```js
const fs = require('fs');
fs.readFile('path/to/file.json', (err, data) => {
  if (err) throw err;
  const jsonData = JSON.parse(data);
  // do something with the data
});
```
