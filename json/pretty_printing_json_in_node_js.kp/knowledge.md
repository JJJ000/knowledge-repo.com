---
title: What is the best way to format JSON output using node.js?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can pretty-print JSON using the `JSON.stringify()` method in node.js.
---

**Contents**

[TOC]

### Using `JSON.stringify()`

The `JSON.stringify()` method can be used to pretty-print JSON in node.js. This method takes two arguments, the first one being the data to be stringified and the second one being an optional replacer function. The replacer function can be used to modify the output by specifying the number of spaces to use for indentation.

For example: 

```js
let data = {
  name: 'John',
  age: 30
};

let prettyData = JSON.stringify(data, null, 2);
console.log(prettyData);
```

This will output the following:

```json
{
  "name": "John",
  "age": 30
}
```

### Using `json-pretty-html`

The `json-pretty-html` package can also be used to pretty-print JSON in node.js. This package can be installed using the following command:

```
npm install json-pretty-html
```

Once the package is installed, it can be used as follows:

```js
let data = {
  name: 'John',
  age: 30
};

let prettyData = jsonPrettyHtml(data);
console.log(prettyData);
```

This will output the following:

```html
<div class="json-pretty-html">
  <span class="json-pretty-html__key">"name"</span>:
  <span class="json-pretty-html__string">"John"</span>,
  <span class="json-pretty-html__key">"age"</span>:
  <span class="json-pretty-html__number">30</span>
</div>
```

### Using `js-beautify`

The `js-beautify` package can also be used to pretty-print JSON in node.js. This package can be installed using the following command:

```
npm install js-beautify
```

Once the package is installed, it can be used as follows:

```js
let data = {
  name: 'John',
  age: 30
};

let prettyData = beautify(data, { indent_size: 2 });
console.log(prettyData);
```

This will output the following:

```json
{
  "name": "John",
  "age": 30
}
```
