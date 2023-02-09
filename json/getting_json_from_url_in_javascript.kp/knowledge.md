---
title: What is the process for retrieving JSON data from a url using javascript?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the built-in fetch API to make a GET request to the URL and parse the response as JSON.
---

**Contents**

[TOC]

# Section 1: Fetching the JSON

Using the `fetch()` API, you can easily fetch the JSON from a URL. Here is an example of how to do this:

```js
fetch('http://example.com/data.json')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

# Section 2: Parsing the JSON

Once you have the JSON data, you can parse it using the `JSON.parse()` method. Here is an example of how to do this:

```js
const jsonData = '{"name":"John","age":30}';
const data = JSON.parse(jsonData);

console.log(data.name); // Outputs "John"
```

# Section 3: Accessing the Data

Once you have parsed the JSON data, you can access it using dot notation or bracket notation. Here is an example of how to do this:

```js
const data = {
  name: 'John',
  age: 30
};

console.log(data.name); // Outputs "John"
console.log(data['age']); // Outputs 30
```

# Section 4: Error Handling

It is important to always handle errors when working with JSON data. Here is an example of how to do this:

```js
fetch('http://example.com/data.json')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(err => console.log('Error:', err));
```
